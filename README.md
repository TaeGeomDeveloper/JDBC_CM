# JDBC_CM
자바에서 제공하는 데이터베이스 와 연결하여 데이터를 주고 받을수 있도록 하는 인터페이스.

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

### Connection close
``` java
   public static void closeConnection(ResultSet rs, Statement stmt, Connection con) {
        if (rs != null) {
            try {
                rs.close();
            } catch (SQLException e) {
                throw new RuntimeException(e);
            }
        }
        if (stmt != null) {
            try {
                stmt.close();
            } catch (SQLException e) {
                throw new RuntimeException(e);
            }
        }
        if (con != null) {
            try {
                con.close();
            } catch (SQLException e) {
                throw new RuntimeException(e);
            }
        }
    }

```
