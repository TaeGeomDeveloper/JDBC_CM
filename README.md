# JDBC_CM

## ConnectionManager

### Connection 연결
``` java
  public static Connection getConnection() {
    Connection con = null;
  
    return con;
  }
```

### Connection 정보 초기화
``` java
  String driver = "com.mysql.cj.jdbc.Driver";
  String jdbcURL = "jdbc:mysql://localhost:3306/gisa";
  String id = "root";
  String pwd = "1234";
```

