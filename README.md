# datasource-test-demo
Hikari
load property file to set config 
set config by programming
spring-boot-starter

HikariConfig configuration = new HikariConfig(properties);
            HikariDataSource hikariDataSource = new HikariDataSource();
            hikariDataSource.setUsername("");
            hikariDataSource.setPassword("");
            hikariDataSource.setJdbcUrl("jdbc:mysql://:3306/demo?useUnicode=true&characterEncoding=utf8");
            hikariDataSource.setPoolName("DatebookHikariCP");
            
property file
jdbcUrl=jdbc:mysql://:3306/demo?useUnicode=true&characterEncoding=utf8
username=
password=
driverClassName=com.mysql.jdbc.Driver
minimumIdle=5
maximumPoolSize=50
idleTimeout=30000
poolName=DatebookHikariCP
maxLifetime=1800000
connectionTimeout=30000
connectionTestQuery=SELECT 1
Properties properties = new Properties();
InputStream is = new FileInputStream("hikariConfig.properties");
properties.load(is);
HikariConfig configuration = new HikariConfig(properties);
