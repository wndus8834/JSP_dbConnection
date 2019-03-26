## JSP_dbConnection

![ezgif-2-c8728f4a71c2](https://user-images.githubusercontent.com/38427658/55024436-2fb58680-5042-11e9-807f-34dd00f21eda.gif)


1.mysql_connector.jar 파일을 프로젝트에 첨부한다.


2. DatabaseUtil.java 파일을 만들어 JSP 프로젝트와 MySQL 데이터를 연결한다.

```java
public static Connection getConnection() {
		try {
			String dbURL="jdbc:mysql://localhost/tutorial?autoReconnect=true&useSSL=false";
			String dbID="root";
			String dbPassword="root";
			Class.forName("com.mysql.jdbc.Driver");
			return DriverManager.getConnection(dbURL, dbID, dbPassword);
		}catch(Exception e) {
			e.printStackTrace();
		}
		return null;
	}
```