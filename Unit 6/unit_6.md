># **Unit - 6 : Database Maintenance and Performance Management**

## 6.1 **Database Maintenance** :

### **Overview** :

Database maintenance encompasses a range of activities aimed at ensuring the smooth operation, security, and reliability of a database system. 
Database maintenance is a critical aspect of managing databases effectively to ensure optimal performance, reliability, and security.

---
   ### **View the Alert Log** :

   * The alert log is a text file that records important database events, including errors, warnings, and startup/shutdown activities.
   * To view the alert log, locate its file path using SQL*Plus: `SHOW PARAMETER BACKGROUND_DUMP_DEST;`.
   * Use any text editor (like Notepad on Windows or vi on Unix/Linux) to open and view the contents of the alert log.
   * Regularly reviewing the alert log is crucial for identifying and troubleshooting database issues.

 ***

   ### **The Automatic Workload Repository(AWR)** : 

   * AWR collects and maintains a historical repository of performance statistics for Oracle databases.
   * It gathers data on database metrics such as CPU usage, memory usage, I/O statistics, and wait events.
   * AWR snapshots are captured at regular intervals (typically every hour) and retained for a configurable retention period.
   * You can generate AWR reports using SQL queries (`DBMS_WORKLOAD_REPOSITORY` package) or through Oracle Enterprise Manager.

   ***

   ### **Statistic Levels** : 

   * Oracle databases offer different levels of statistics gathering: basic, typical, and all.
   * `STATISTICS_LEVEL` parameter controls the level of statistics gathering.
   * Basic level gathers minimal statistics, typical level gathers moderate statistics, and all level gathers comprehensive statistics.
   * Increasing the statistics level incurs additional overhead but provides more detailed performance data.

   ***

   ### **The Automatic Database Diagnostic Monitoring(ADDM)** : 
   * ADDM analyzes AWR data to identify performance issues and provide recommendations for resolution.
   * It automatically runs during AWR snapshot generation and generates findings reports.
   * ADDM examines database performance across various dimensions, such as CPU, memory, I/O, and SQL execution.
   * Recommendations provided by ADDM assist database administrators in addressing performance bottlenecks and improving database efficiency.

   ***

   ### **Monitor an Oracle Database** :

   * Oracle Enterprise Manager (OEM) is a centralized management tool for monitoring Oracle databases.
   * OEM provides a graphical interface for monitoring database health, performance metrics, and system alerts.
   * It offers customizable dashboards, performance charts, and reports for real-time monitoring and analysis.
   * DBAs can configure thresholds and notifications to receive alerts via email or SMS for critical database events.

   ***

   ### **Use the Advisors** : 

   * Oracle Database includes several advisors that provide expert recommendations for database tuning and maintenance.
   * SQL Tuning Advisor analyzes SQL statements and suggests improvements for better performance.
   * Segment Advisor identifies space usage and fragmentation issues in database segments.
   * Memory Advisor recommends memory configuration changes to optimize database performance.
   * DBAs can invoke these advisors manually through Oracle Enterprise Manager or using SQL commands.

***

   ### **Set Up Notification Rules** :

   * Oracle Enterprise Manager allows DBAs to define notification rules for alerting on critical events.
   * Notification rules specify conditions based on metrics thresholds or specific events.
   * DBAs can configure notification channels (email, SMS, SNMP) and recipients for each rule.
   * Notifications provide timely alerts to DBAs, enabling proactive monitoring and rapid response to database issues.

***

## 6.2 **Performance Management** :

Performance management in the context of Oracle involves the systematic process of optimizing the performance of Oracle database systems to ensure efficient operation and meet business requirements.

---

### **Tuning Information Sources** :

Tuning information sources in performance management refers to enhancing the quality, relevance, and accessibility of data used to assess and improve performance.


"Tuning Information Sources" refers to the various sources of data and insights that database administrators and performance engineers utilize to diagnose and optimize the performance of Oracle database systems. These sources provide valuable information about system behavior, resource utilization, and performance metrics, enabling informed tuning decisions.

***

### **Performance Monitoring** :


Performance monitoring in Oracle involves the continuous observation and analysis of various system metrics and parameters to ensure optimal database performance. Administrators utilize tools like Oracle Enterprise Manager (OEM), Automatic Workload Repository (AWR), and dynamic performance views to collect data on key metrics such as CPU utilization, memory usage, I/O throughput, and SQL execution statistics. By monitoring in real-time and analyzing historical data, they can identify performance anomalies, pinpoint areas of contention or bottlenecks, and take proactive measures to optimize resource utilization and maintain system efficiency. Additionally, performance monitoring supports capacity planning efforts, enabling organizations to forecast future requirements and ensure adequate provisioning to meet growing demands. By continuously refining monitoring strategies and incorporating feedback, organizations can improve the reliability, scalability, and performance of their Oracle database environments over time.

***

### **Tuning Activities** :

Tuning activities in Oracle involve a series of optimizations aimed at improving the performance and efficiency of database systems. This includes tasks such as optimizing database indexes and SQL queries, managing memory allocation, configuring storage for optimal I/O performance, adjusting database parameters, managing SQL execution plans, implementing table and index partitioning, collecting and maintaining statistics, optimizing application design, and conducting performance testing and validation. By systematically addressing these areas, administrators can enhance the performance, scalability, and reliability of Oracle database environments to meet business needs and deliver optimal user experiences.

***


### **Performance Planning** :

Performance planning in Oracle involves strategizing to ensure that database systems operate efficiently and effectively to meet business needs. This includes setting performance goals aligned with business objectives, defining key performance indicators (KPIs) to measure success, establishing benchmarks for comparison, and planning capacity scaling based on workload analysis and growth forecasts. Administrators also assess potential risks and vulnerabilities, evaluate new technologies for performance improvements, and continuously monitor and report on performance metrics to track progress and identify areas for optimization. By engaging in comprehensive performance planning, organizations can proactively address performance challenges and optimize Oracle database systems to support business operations effectively.

***

### **Instance Tuning** :

Instance tuning in Oracle focuses on optimizing the configuration and behavior of database instances to enhance performance and resource utilization. This involves adjusting parameters related to memory allocation, CPU utilization, and I/O operations to ensure efficient operation of the database. Additionally, instance tuning includes managing automatic memory and shared memory allocation, optimizing optimizer statistics, configuring instance recovery settings, and implementing resource management policies. Continuous monitoring and analysis of instance performance help identify areas for improvement and fine-tune configuration settings to meet changing workload demands effectively.

***

### **Performance Tuning Methodology** :

Performance tuning methodology in Oracle involves a structured approach to optimizing the performance of database systems and applications. It begins with analyzing the current performance, identifying performance goals aligned with business requirements, and establishing benchmarks for comparison. Next, performance bottlenecks are identified through analysis of system components, resource utilization, and wait events. Root cause analysis is performed to understand underlying reasons for performance issues, followed by the implementation of targeted tuning interventions such as optimizing SQL queries, adjusting database parameters, or redesigning database schemas. Performance validation is conducted through testing and validation to ensure that tuning changes meet performance goals. The process is iterative, with continuous monitoring, analysis, and fine-tuning to achieve incremental improvements over time. Documentation, knowledge sharing, and proactive monitoring and maintenance practices are essential for sustaining optimal performance.

***

### **Performance Tuning Data** :

Performance tuning data in Oracle encompasses various metrics such as wait events, SQL statements, system and session statistics, buffer cache and PGA statistics, index usage, and database workload. By analyzing these metrics, administrators can pinpoint bottlenecks, optimize resource utilization, and improve overall system performance. This data provides insights into the database's behavior, helping to identify inefficient queries, memory allocation issues, and areas for indexing improvements. Overall, leveraging performance tuning data enables organizations to fine-tune their Oracle databases for optimal performance and efficiency.

***

### **Monitoring Performance** :


Monitoring performance in Oracle is a proactive process where administrators keep a close eye on critical aspects of the database environment. They use tools such as Oracle Enterprise Manager to track key metrics like CPU usage, memory utilization, and disk I/O in real-time. By analyzing this data, they can detect any anomalies or performance bottlenecks and take corrective actions promptly. Additionally, administrators monitor SQL statement execution, index usage, and database workload to optimize system performance continuously. This approach helps ensure that Oracle databases operate smoothly and efficiently, meeting the needs of users and applications effectively.


***


### **Managing Memory** :


Managing memory in Oracle involves efficiently allocating and monitoring memory resources to optimize database performance. Administrators configure parameters such as SGA (System Global Area) and PGA (Program Global Area) to allocate memory for database operations. They monitor memory usage using tools like Oracle Enterprise Manager to ensure resources are utilized effectively and to prevent performance issues such as excessive swapping or memory leaks. Regular performance tuning and capacity planning help maintain optimal memory utilization and support the smooth operation of Oracle databases.


***

### **Manage Private Temporary Tables** :

Managing private temporary tables in Oracle involves creating temporary tables that are session-specific and automatically dropped at the end of the session. These tables are useful for storing intermediate results or temporary data within a specific session.

Private temporary tables in Oracle are created with the `CREATE PRIVATE TEMPORARY TABLE` statement, allowing users to store temporary data within a session. These tables are session-specific, meaning they are only accessible within the session in which they are created. They automatically drop at the end of the session, freeing up resources and eliminating the need for manual cleanup. Private temporary tables can be manipulated like regular tables, making them useful for storing intermediate results or temporary data during complex operations or transactions. Their automatic cleanup feature simplifies management and ensures efficient resource utilization in Oracle databases.
