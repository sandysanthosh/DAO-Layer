Welcome to the DAO-Layer wiki!



public class studentDAO{
 private DataSourceds;
public arraylist<student getAllStudent(){
ArrayList<Student> list=new ArrayList<Student>();
String sql="select * from student";
ResultSet rs=executeFetchQuery(sql);
try{
while(rs.next())
{
student student=new student();
student.setStudentID(rs.getString("STUDENTID"));
student.setName(rs.getString("Name"));
student.setAdrress(rs.getString("Address"));
list.add(student);
}
catch(Exception e)
{
System.err.println("GS"+ex.getMessage());
}


public void deleteStudent(Student student){
String sql="delete from student where studentid=""+ student.getStudentID() + "'";
executeModifyQuery(sql);
}

public void editStduent(Student student){
String sql="update student set name='"+student.getName()+"',Address='"+student.getAddress()+"' where studentID='" ;
executeModifyQuery(sql);
}

return student;
}

public void addStudent(Student student){
String sql="Insert into student values('"+student.getString() +'" + student.getAddress()+"')";
executeModifyQuery(sql);
}
}

public void executeModifyQuery(String sql){
try{
Connection conn=ds.getConnection();
conn.createStatement().execuse(sql);
conn.close();
}catch(Exception e){
System.err.println(e.getMessage());
}
}



public void executeModifyQuery(String sql){
try{
Connection conn=ds.getConnection();
conn.createStatement().execuse(sql);
conn.close();
}catch(Exception e){
System.err.println(e.getMessage());
}
}


public ResultsetexecuteFetchQuery(String sql){
ResultSet rs=null;
try{
Connection conn=ds.getConnection();
conn.createStatement().execuse(sql);
conn.close();
}catch(Exception e){
System.err.println(e.getMessage());
}
return rs;
}




AllStudent.java:

processRequets(request,response)
{
private studentDAO studentDAO;
ArrayList<Stduent> list=StudentDAO.getallstudent();
request.setAttribute("list",list);
request.getRequestDispatcher("allstudent.jsp").forward(request,response);
}
}









