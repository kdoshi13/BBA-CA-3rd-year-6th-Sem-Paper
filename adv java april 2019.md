1.
Answer the following (any eight) :
[8×2=16]
 
(i)
What is jdbc-api ?
=)The JDBC API (Java Database Connectivity API) is a Java API for connecting and interacting with databases.
It provides a standard way to execute SQL statements and retrieve data from relational databases.
Using JDBC, Java applications can establish connections, create statements, execute queries, and process results.
It acts as a bridge between Java and different database systems, allowing developers to write database-independent code.
JDBC enables storing and retrieving data, performing transactions, and managing database connections.
It is a convenient and flexible tool for working with databases in Java applications.
 
(ii)
What is Servlet Config ?
=)
The `ServletConfig` interface in Java Servlets provides a way to initialize and configure a servlet. It allows servlets to access initialization parameters defined in the web application's deployment descriptor (web.xml) or programmatically during servlet initialization. The `ServletConfig` object is unique to each servlet and is created by the servlet container. Servlets can use the `ServletConfig` methods, such as `getInitParameter()` and `getServletContext()`, to retrieve initialization parameters and obtain the servlet context, respectively. This information can be useful for customizing the behavior of a servlet based on configuration settings.
 
(iii)
What is accept() method in networking ?
=)The `accept()` method is a method provided by the Java networking classes, such as `ServerSocket` or `SocketServer`. This method is used in server-side programming to accept incoming client connections. 

When a server socket is created and bound to a specific port, the `accept()` method is called to wait for a client to initiate a connection. It blocks the execution of the server program until a client connects to the server. Once a client connection is received, the `accept()` method returns a new `Socket` object representing the connection to the client.

The `accept()` method is typically used in a loop to continuously accept multiple client connections. Once a connection is accepted, the server can then perform various operations, such as sending and receiving data, with the connected client through the `Socket` object returned by `accept()`.
 
(iv)
What is sleep() method ?
=)The `sleep()` method is a method provided by the `Thread` class in Java. It allows a thread to pause its execution for a specified amount of time. 

When `sleep()` is called, the thread enters a sleeping state, temporarily suspending its execution. This is useful in scenarios where a thread needs to wait for a certain period of time before proceeding with its tasks. 

The `sleep()` method takes a parameter that specifies the duration of sleep in milliseconds. For example, `Thread.sleep(2000)` would cause the current thread to sleep for 2 seconds.

It's important to note that the `sleep()` method can throw an `InterruptedException` if the thread is interrupted while sleeping. This exception can be caught and handled if necessary.

Using `sleep()` can be helpful for tasks such as adding delays, implementing timeouts, or coordinating actions between threads. However, it's important to use it judiciously, considering the impact on system resources and overall program flow.
 
(v)
Give syntax of loading Driver Manager.
=)To load the JDBC driver using the `DriverManager` class in Java, you can use the following syntax:

```java
Class.forName("com.mysql.jdbc.Driver");
```

In the above example, `"com.mysql.jdbc.Driver"` is the fully qualified class name of the JDBC driver you want to load. This example assumes that you are loading the MySQL JDBC driver.

By calling `Class.forName("com.mysql.jdbc.Driver")`, you instruct the Java runtime to load and register the specified JDBC driver. The `forName()` method dynamically loads the driver class into memory, allowing you to establish a connection to the corresponding database.

It's important to note that starting from JDBC 4.0, the driver loading step is not strictly necessary as long as the driver is present in the classpath. However, for older versions or specific driver requirements, loading the driver explicitly using `Class.forName()` is still commonly used.
 
(vi)
Define Port.
=)In computer networking, a port refers to a logical construct that allows multiple applications or processes to communicate over a network. It acts as an endpoint for communication, enabling the identification of specific services or applications running on a device.

Ports are numbered from 0 to 65535 and are divided into three ranges: well-known ports (0-1023), registered ports (1024-49151), and dynamic or private ports (49152-65535).

Well-known ports are assigned to specific services, such as port 80 for HTTP (Hypertext Transfer Protocol) or port 22 for SSH (Secure Shell). Registered ports are typically used by software applications for specific purposes. Dynamic or private ports are usually chosen dynamically by the operating system for temporary communication between client and server.

When a network communication occurs, the combination of an IP address and a port number identifies the specific destination or source for the data being exchanged. This allows multiple applications on a single device to receive and handle network traffic independently.

In summary, a port is a numbered endpoint that enables communication between applications or services over a network, facilitating the delivery of data to the appropriate software or process running on a device.
 
(vii)
What is yield() method ?
=)The `yield()` method is a method provided by the `Thread` class in Java. It is used to voluntarily give up the current thread's processor time to allow other threads of equal or higher priority to run. When a thread calls `yield()`, it temporarily pauses its execution and goes back to the ready state. The thread scheduler then decides which thread to execute next. If there are no other threads of equal or higher priority waiting to run, the same thread may continue its execution. Using `yield()` is a way to indicate that the current thread is willing to yield its time to other threads, promoting fairness and cooperation among threads. However, it's important to note that the actual behavior of `yield()` depends on the underlying operating system and thread scheduler.
 
(viii) What is Stub and skeleton ?
=)In distributed computing and remote procedure call (RPC), a stub and a skeleton are components used to facilitate communication between a client and a server.

A stub, also known as a client stub or proxy, is a client-side component that acts as a representative or proxy for the actual server object. The client interacts with the stub as if it were the real server object, making method calls on the stub. The stub then marshals (converts) the method parameters into a format suitable for network transmission and sends the request over the network to the server.

On the server side, the skeleton, also known as a server stub, is responsible for receiving the requests from the network, unmarshalling the parameters, and invoking the actual server object's methods. It acts as an intermediary between the network and the server object, handling the communication details.

In summary, the stub is used on the client side to represent the server object and handle the communication with the server, while the skeleton is used on the server side to receive requests, unmarshal parameters, and invoke the appropriate server object's methods. These components work together to enable remote method invocation and communication between distributed systems.
 
(ix)
What is Scriptlet tag ?
=)In JavaServer Pages (JSP), a scriptlet tag is a construct that allows you to embed Java code directly into the JSP page. It is represented by the `<% %>` tags.

Inside the scriptlet tag, you can write arbitrary Java code, including variable declarations, control structures (if-else, loops), method invocations, and more. The code within the scriptlet is executed on the server-side when the JSP page is processed.

Here's an example of a scriptlet tag that prints "Hello, World!" on a JSP page:

```jsp
<html>
<body>
<%
    String message = "Hello, World!";
    out.println(message);
%>
</body>
</html>
```

In the above example, the `<% %>` tags contain the Java code that assigns the message variable with the string "Hello, World!" and then uses the `out` object (provided by JSP) to output the message on the page.

It's important to note that although scriptlet tags provide flexibility, it's generally recommended to separate the business logic from the presentation layer in JSP by using JavaBeans or servlets for complex processing, and using JSP for rendering the output.
(x)
What is builder tool ?
=)A builder tool, in the context of software development, refers to a software utility or framework that helps streamline and simplify the process of building or constructing software applications. It provides a structured approach to defining and managing the build process, automating repetitive tasks, and ensuring consistent and reliable builds.

Some common features and capabilities of builder tools include:

1. Compilation: Automating the compilation of source code files into executable binaries or intermediate representations.

2. Dependency Management: Managing dependencies between different components or libraries used in the application, ensuring that all required dependencies are properly included.

3. Packaging: Creating distributable packages or artifacts that bundle the application and its dependencies for deployment or distribution.

4. Testing: Supporting the execution of tests, such as unit tests or integration tests, to ensure the quality and correctness of the software.

5. Continuous Integration/Continuous Delivery (CI/CD): Integrating with CI/CD pipelines to automate the build, testing, and deployment processes.

Examples of popular builder tools in the Java ecosystem include Apache Maven, Gradle, and Ant. These tools provide build configurations, plugins, and a command-line interface or build scripts to define and control the build process effectively.

By using a builder tool, developers can simplify the build process, improve productivity, maintain consistency across different environments, and automate repetitive tasks, ultimately facilitating the development and delivery of high-quality software applications.
Q2.
Answer the following (any four) :
[4×4=16]
(a)
Explain difference between Statements and Prepared Statement.
=)Statements and PreparedStatements are two types of SQL execution interfaces in Java that allow you to interact with databases. Here's the difference between them:

1. Execution Process:
   - Statements: When a statement is executed, the SQL query is sent to the database, compiled, and executed. This process happens each time the statement is executed.
   - PreparedStatements: PreparedStatements follow a two-step execution process. First, the SQL query is sent to the database and precompiled. Then, when the statement is executed, only the parameter values are sent to the database, allowing for efficient execution.

2. Compilation:
   - Statements: Statements are compiled and executed each time they are invoked. The database engine needs to parse and compile the SQL query repeatedly, which can impact performance.
   - PreparedStatements: PreparedStatements are precompiled only once during their creation. The compiled form of the query is cached by the database, allowing for faster subsequent executions.

3. Parameter Binding:
   - Statements: Statements do not inherently support parameter binding. If you have parameters in your SQL query, you need to concatenate them as strings, which may lead to security vulnerabilities like SQL injection if not handled carefully.
   - PreparedStatements: PreparedStatements provide built-in support for parameter binding. You can set parameters using placeholder symbols in the SQL query, and the PreparedStatement ensures proper parameter handling and prevents SQL injection attacks.

4. Performance:
   - Statements: Due to the compilation overhead for each execution, Statements may be less efficient when executing the same query multiple times with different values.
   - PreparedStatements: PreparedStatements offer better performance when executing the same query multiple times with different values since the compilation step is performed only once.

5. Security:
   - Statements: Statements are more prone to SQL injection attacks if input values are concatenated directly into the query string.
   - PreparedStatements: PreparedStatements, with their parameter binding feature, provide a built-in mechanism to prevent SQL injection by properly handling input values.

In summary, PreparedStatements offer advantages in terms of performance, security, and reusability. They are particularly useful when executing the same query multiple times with different parameter values. Statements, on the other hand, are simpler and suitable for basic SQL operations but lack the efficiency and security features provided by PreparedStatements.
(b)
What is Thread ? Explain different ways to implement thread
in program.
=)A thread is a lightweight unit of execution within a program. It represents an independent flow of control that can perform tasks concurrently with other threads. Threads allow programs to execute multiple operations simultaneously, thereby enabling concurrent and parallel processing.

In Java, there are two main ways to implement threads in a program:

1. Extending the Thread class:
   - The first way is to create a new class that extends the `Thread` class. This class can override the `run()` method, which contains the code that will be executed in the thread. The `run()` method represents the entry point of the thread's execution. Once the class is defined, an instance of it can be created and started by calling the `start()` method.

2. Implementing the Runnable interface:
   - The second way is to implement the `Runnable` interface. This interface defines a single method called `run()`. The class implementing `Runnable` needs to provide an implementation of this method. Once implemented, an instance of the class can be passed as an argument to the `Thread` constructor or a `Thread` object can be created with the `Runnable` implementation, and then the thread can be started by calling the `start()` method.

Here's an example of each approach:

1. Extending the Thread class:
```java
class MyThread extends Thread {
    public void run() {
        // Code to be executed in the thread
    }
}

// Create and start the thread
MyThread thread = new MyThread();
thread.start();
```

2. Implementing the Runnable interface:
```java
class MyRunnable implements Runnable {
    public void run() {
        // Code to be executed in the thread
    }
}

// Create a Runnable instance and pass it to Thread constructor
MyRunnable runnable = new MyRunnable();
Thread thread = new Thread(runnable);
thread.start();
```

Both approaches allow you to execute code concurrently in separate threads. Choosing between them depends on the specific requirements and design of your program. Implementing the `Runnable` interface is often preferred as it allows for better separation of concerns and easier resource sharing between threads.

(c)
Explain RMI Architecture with a suitable diagram.
=)RMI is a Java-based technology that enables communication between distributed systems by allowing objects in one Java Virtual Machine (JVM) to invoke methods on objects residing in another JVM. It provides a mechanism for remote communication and method invocation, making distributed computing transparent to the developer.

The RMI architecture involves the following components:

1. Remote Interface:
   - The remote interface defines the methods that can be invoked remotely. It extends the `java.rmi.Remote` interface and declares the remote methods that can be accessed by clients.

2. Remote Object:
   - The remote object implements the remote interface and provides the actual implementation for the remote methods. It extends the `java.rmi.server.UnicastRemoteObject` class to enable remote invocation.

3. Stub:
   - The stub acts as a proxy for the remote object on the client side. It resides in the client's JVM and provides a local representation of the remote object. The stub handles the communication details with the remote object and marshals parameters and results between the client and server.

4. Skeleton:
   - The skeleton resides in the server's JVM and acts as an intermediary between the stub and the remote object. It receives method invocations from the stub, unmarshals parameters, and invokes the corresponding methods on the remote object.

5. RMI Registry:
   - The RMI registry is a centralized registry that keeps track of remote objects. Clients can locate remote objects by querying the registry using a logical name associated with the object.

The interaction between these components can be summarized as follows:

1. The client requests a reference to the remote object from the RMI registry.
2. The RMI registry returns a stub object to the client.
3. The client invokes methods on the stub as if it were invoking local methods.
4. The stub marshals the method name and parameters and sends them to the server.
5. The skeleton receives the request on the server side, unmarshals the parameters, and invokes the corresponding method on the remote object.
6. The remote object executes the method and returns the result.
7. The skeleton marshals the result and sends it back to the client.
8. The stub receives the result, unmarshals it, and returns the result to the client.
https://www.tutorialspoint.com/java_rmi/images/rmi_architecture.jpg
(d)
Write a JDBC Program to delete the record of employee using
command line argument.
=)
```java
import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.SQLException;
import java.sql.Statement;

public class DeleteEmployee {
    public static void main(String[] args) {
        if (args.length != 1) {
            System.out.println("Usage: java DeleteEmployee <employee_id>");
            return;
        }

        int employeeId = Integer.parseInt(args[0]);

        try {
            // Step 1: Establish the database connection
            Connection connection = DriverManager.getConnection("jdbc:mysql://localhost:3306/your_database", "username", "password");

            // Step 2: Create a SQL statement
            Statement statement = connection.createStatement();

            // Step 3: Execute the SQL statement
            String sql = "DELETE FROM employee WHERE employee_id = " + employeeId;
            int rowsAffected = statement.executeUpdate(sql);

            // Step 4: Process the result
            if (rowsAffected > 0) {
                System.out.println("Record deleted successfully!");
            } else {
                System.out.println("No record found with the given employee ID.");
            }

            // Step 5: Close the resources
            statement.close();
            connection.close();
        } catch (SQLException e) {
            System.out.println("An error occurred while deleting the record: " + e.getMessage());
        }
    }
}
```
(e)
Write a multithreading program in Java using Runnable interface
to draw temple flag on an applet container.
=)
```java
import java.awt.*;
import java.applet.*;
/* <APPLET     code= "flag.class"  width= "500" height= "300">
     </APPLET> */
public class flag extends Applet implements Runnable
{
            Thread t;
            int x1,x2,x3,y3,x4,y4,x5,ln;
            public void init()
            {
                        t=new Thread(this);
                        t.start();
                        ln=1;
            }
            public void run()
            {
            try{      if(ln==1) {         for(x1=200;x1>100;)
                                               {
                                                       t.sleep(200);
                                                       repaint();
                                                }
                                       }
                        ln=2;
                        if(ln==2) {        for(x2=100;x2<150;)
                                                {
                                                          t.sleep(200);
                                                          repaint();
                                                }
                                      }
                        ln=3;
                        if(ln==3) {       for(x3=150,y3=100;x3>125&&y3<125;)
                                               {
                                                      t.sleep(200);
                                                      repaint();
                                              }
                                          }
                        ln=4;
                        if(ln==4) {     for(x4=125,y4=125;x4<150&&y4<150;)
                                            {
                                                t.sleep(200);
                                                repaint();
                                            }
                                       }
                        ln=5;
                        if(ln==5)  {     for(x5=150;x5>100;)
                                             {
                                                t.sleep(200);
                                                repaint();
                                              }
                                        }
                        ln=1;
            }catch(Exception e){
                                                      System.out.println(e);
                                             }
            run();  
            }
            public void paint(Graphics g)
            {
                        if(ln==1&&x1>100)
                        {
                                    g.drawLine(100,200,100,x1-=5);
                        }
                        if(ln==2&&x2<150)
                        {
                                    g.drawLine(100,200,100,100);
                                    g.drawLine(100,100,x2+=5,100);
                        }
                        if(ln==3&&x3>125&&y3<125)
                        {
                                    g.drawLine(100,200,100,100);
                                    g.drawLine(100,100,150,100);
                                    g.drawLine(150,100,x3-=5,y3+=5);
                        }
                        if(ln==4&&x4<150&&y4<150)
                        {
                                    g.drawLine(100,200,100,100);
                                    g.drawLine(100,100,150,100);
                                    g.drawLine(150,100,125,125);
                                    g.drawLine(125,125,x4+=5,y4+=5);
                        }
                        if(ln==5&&x5>100)
                        {
                                    g.drawLine(100,200,100,100);
                                    g.drawLine(100,100,150,100);
                                    g.drawLine(150,100,125,125);
                                    g.drawLine(125,125,150,150);
                                    g.drawLine(150,150,x5-=5,150);
                        }                      
            }
}
```
3.
Answer the following (any four) :
[4×4=16]
(a)
Explain various components of JSP ?
=)JSP (JavaServer Pages) is a technology used for developing dynamic web pages in Java. It allows for the embedding of Java code within HTML content, enabling the creation of dynamic and interactive web applications. The various components of JSP include:

1. Scripting Elements:
   - JSP provides scripting elements to embed Java code within the HTML content of a JSP page. There are three types of scripting elements: scriptlet (`<% %>`) for general Java code, expression (`<%= %>`) for evaluating and displaying the result of an expression, and declaration (`<%! %>`) for defining variables and methods.

2. Directives:
   - JSP directives are instructions for the JSP container on how to process the JSP page. They are used to import classes, define error handling pages, control the page's caching behavior, and more. Directives are defined using the `<%@ directive %>` syntax.

3. Declarations:
   - Declarations allow you to define variables and methods within a JSP page. They are typically used for utility methods, initialization code, or shared variables. Declarations are enclosed within the `<%! %>` tags.

4. Expressions:
   - Expressions are used to evaluate and display the result of a Java expression within the HTML content of a JSP page. They are enclosed within the `<%= %>` tags and can include variables, method invocations, or any valid Java expression.

5. Actions:
   - JSP actions are XML-like tags that perform specific tasks within a JSP page. They provide a convenient way to interact with JavaBeans, manage session attributes, control flow, and more. Some commonly used JSP actions include `<jsp:useBean>`, `<jsp:setProperty>`, `<jsp:getProperty>`, `<jsp:include>`, and `<jsp:forward>`.

6. Standard Tag Library (JSTL):
   - JSTL is a library of custom tags that provides additional functionality for JSP pages. It includes tags for conditional statements, looping, internationalization, formatting, database access, and more. The JSTL tags allow for cleaner and more modular JSP code.

7. Expression Language (EL):
   - The Expression Language is a simplified language for accessing and manipulating data within a JSP page. It provides a convenient syntax for retrieving and setting attribute values, invoking methods, performing arithmetic operations, and accessing collections. EL expressions are enclosed within `${}` tags.

8. Implicit Objects:
   - JSP provides a set of predefined objects called implicit objects that can be accessed directly within the JSP page without explicitly declaring them. Examples of implicit objects include `request`, `response`, `session`, `application`, `out`, `pageContext`, and more. These objects provide access to request parameters, session attributes, response output, and other web-related functionality.

(b)
What is JAR file ? Explain steps to create it.
=)A JAR (Java Archive) file is a file format used to package multiple Java class files, resources, and metadata into a single compressed file. It is commonly used for distributing Java libraries, applications, or modules, as it simplifies the packaging, distribution, and deployment of Java components.

To create a JAR file, you can follow these steps:

1. Compile your Java source code:
   - Before creating a JAR file, ensure that you have compiled your Java source code (.java files) into bytecode (.class files) using the Java compiler (`javac`). This step generates the necessary compiled class files that will be included in the JAR file.

2. Create a manifest file (optional):
   - A manifest file is an optional metadata file that can be included in the JAR file. It contains information about the JAR file and its contents. If you want to specify a custom manifest file, create a text file (e.g., `manifest.txt`) and include the necessary attributes, such as the main class, classpath dependencies, etc. Each attribute should be on a separate line. Make sure to include a newline character at the end of the file.

3. Package the files into a JAR file:
   - Open a command prompt or terminal and navigate to the directory containing your compiled class files and manifest file (if any). Use the `jar` command provided by the Java Development Kit (JDK) to create the JAR file. The basic syntax is as follows:
   ```
   jar cf jar-file input-file(s)
   ```
   - `jar-file` is the name of the JAR file you want to create, and `input-file(s)` are the files and directories that you want to include in the JAR file. You can specify multiple files and directories, separating them with spaces.
   - If you have a custom manifest file, you can specify it using the `-m` option:
   ```
   jar cfm jar-file manifest-file input-file(s)
   ```
   - Example:
   ```
   jar cf mylibrary.jar com/example/*.class
   ```

4. Verify the JAR file:
   - After creating the JAR file, you can verify its contents by using the `jar` command with the `-t` option:
   ```
   jar tf jar-file
   ```
   - This will display a list of files and directories contained within the JAR file.

5. Use the JAR file:
   - Once the JAR file is created, you can use it in your Java applications by including it in the classpath. You can run Java programs that depend on the classes in the JAR file by specifying the JAR file in the classpath using the `-cp` or `-classpath` option when running the `java` command.

(c)
Explain Inter Thread Communication in Multithreading.
=)Inter-thread communication or Co-operation is all about allowing synchronized threads to communicate with each other.

Cooperation (Inter-thread communication) is a mechanism in which a thread is paused running in its critical section and another thread is allowed to enter (or lock) in the same critical section to be executed.It is implemented by following methods of Object class:

wait()
notify()
notifyAll()
1) wait() method
The wait() method causes current thread to release the lock and wait until either another thread invokes the notify() method or the notifyAll() method for this object, or a specified amount of time has elapsed.

The current thread must own this object's monitor, so it must be called from the synchronized method only otherwise it will throw exception.

Method	Description
public final void wait()throws InterruptedException	It waits until object is notified.
public final void wait(long timeout)throws InterruptedException	It waits for the specified amount of time.
2) notify() method
The notify() method wakes up a single thread that is waiting on this object's monitor. If any threads are waiting on this object, one of them is chosen to be awakened. The choice is arbitrary and occurs at the discretion of the implementation.

Syntax:

public final void notify()  
3) notifyAll() method
Wakes up all threads that are waiting on this object's monitor.

Syntax:

public final void notifyAll()  
(d)
Write a JDBC Program to Insert the record into patient table
(use prepared Statement).
=)
```java
import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.PreparedStatement;
import java.sql.SQLException;

public class InsertPatient {
    public static void main(String[] args) {
        // Database connection details
        String url = "jdbc:mysql://localhost:3306/your_database";
        String username = "your_username";
        String password = "your_password";

        // Patient details for insertion
        String name = "John Doe";
        int age = 30;
        String address = "123 Main Street";
        String diagnosis = "Fever";

        try {
            // Step 1: Establish the database connection
            Connection connection = DriverManager.getConnection(url, username, password);

            // Step 2: Create a prepared statement
            String sql = "INSERT INTO patient (name, age, address, diagnosis) VALUES (?, ?, ?, ?)";
            PreparedStatement statement = connection.prepareStatement(sql);

            // Step 3: Set the parameter values
            statement.setString(1, name);
            statement.setInt(2, age);
            statement.setString(3, address);
            statement.setString(4, diagnosis);

            // Step 4: Execute the statement
            int rowsAffected = statement.executeUpdate();

            // Step 5: Process the result
            if (rowsAffected > 0) {
                System.out.println("Record inserted successfully!");
            } else {
                System.out.println("Failed to insert record.");
            }

            // Step 6: Close the resources
            statement.close();
            connection.close();
        } catch (SQLException e) {
            System.out.println("An error occurred while inserting the record: " + e.getMessage());
        }
    }
}

```
(e)
Write a JSP Program to accept user and check whether it is prime or not.
=)
```jsp
<%@ page language="java" %>
<html>
<head>
    <title>Prime Number Checker</title>
</head>
<body>
    <h1>Prime Number Checker</h1>
    <form method="post" action="primeCheck.jsp">
        Enter a number: <input type="number" name="number" required>
        <input type="submit" value="Check">
    </form>

    <%-- JSP Scriptlet --%>
    <%!
        // Function to check whether a number is prime
        public boolean isPrime(int number) {
            if (number <= 1) {
                return false;
            }

            // Check for divisibility from 2 to square root of the number
            for (int i = 2; i <= Math.sqrt(number); i++) {
                if (number % i == 0) {
                    return false;
                }
            }

            return true;
        }
    %>

    <%-- JSP Java Code --%>
    <%!
        // Get the number input from the form submission
        int number = Integer.parseInt(request.getParameter("number"));

        // Check if the number is prime
        boolean isPrime = isPrime(number);
    %>

    <%-- JSP HTML Output --%>
    <h2>Result:</h2>
    <% if (isPrime) { %>
        <p><%= number %> is a prime number.</p>
    <% } else { %>
        <p><%= number %> is not a prime number.</p>
    <% } %>
</body>
</html>
```
4.
Answer the following (any four) :
[4×4=16]
(a)
Explain different types of servlet with an example.
=)Certainly! There are three types of servlets in Java based on their purpose and functionality:

1. GenericServlet:
   - `GenericServlet` is the base class for all servlets and provides a generic implementation of the `Servlet` interface.
   - It is designed to handle any type of protocol-independent requests and responses.
   - Example: A servlet that handles common tasks like processing form data, file uploads, or sending email notifications.

```java
import java.io.*;
import javax.servlet.*;
import javax.servlet.http.*;

public class GenericServletExample extends GenericServlet {
    public void service(ServletRequest request, ServletResponse response)
            throws ServletException, IOException {
        response.setContentType("text/html");

        PrintWriter out = response.getWriter();
        out.println("<html>");
        out.println("<head><title>GenericServlet Example</title></head>");
        out.println("<body>");
        out.println("<h2>Hello, from GenericServlet!</h2>");
        out.println("</body></html>");

        out.close();
    }
}
```

2. HttpServlet:
   - `HttpServlet` is a subclass of `GenericServlet` specifically designed to handle HTTP requests and responses.
   - It provides methods such as `doGet()`, `doPost()`, `doPut()`, `doDelete()`, etc., to handle specific HTTP methods.
   - Example: A servlet that processes user login, handles form submissions, or implements a RESTful API.

```java
import java.io.*;
import javax.servlet.*;
import javax.servlet.http.*;

public class HttpServletExample extends HttpServlet {
    protected void doGet(HttpServletRequest request, HttpServletResponse response)
            throws ServletException, IOException {
        response.setContentType("text/html");

        PrintWriter out = response.getWriter();
        out.println("<html>");
        out.println("<head><title>HttpServlet Example</title></head>");
        out.println("<body>");
        out.println("<h2>Hello, from HttpServlet!</h2>");
        out.println("</body></html>");

        out.close();
    }
}
```

3. SingleThreadModel:
   - `SingleThreadModel` is an interface that extends the `Servlet` interface and is used to indicate that a servlet is not thread-safe.
   - When a servlet implements this interface, the server guarantees that only one thread will execute the `service()` method of that servlet at a time.
   - Example: A servlet that performs complex calculations or accesses shared resources that require exclusive access.

```java
import java.io.*;
import javax.servlet.*;
import javax.servlet.http.*;

public class SingleThreadModelExample extends HttpServlet implements SingleThreadModel {
    public void service(HttpServletRequest request, HttpServletResponse response)
            throws ServletException, IOException {
        response.setContentType("text/html");

        PrintWriter out = response.getWriter();
        out.println("<html>");
        out.println("<head><title>SingleThreadModel Example</title></head>");
        out.println("<body>");
        out.println("<h2>Hello, from SingleThreadModel!</h2>");
        out.println("</body></html>");

        out.close();
    }
}
```
(b)
Explain Socket and Server Socket.
=)Socket:
A socket is an endpoint for communication between two machines over a network. It represents a connection-oriented communication channel that allows programs to send and receive data. A socket provides a combination of IP address and port number that uniquely identifies a specific process or service running on a machine. It enables communication between clients and servers by establishing a reliable, bidirectional communication channel.

Server Socket:
A server socket is a socket that waits and listens for incoming client connections on a specific port. It is typically used by server applications to accept and handle multiple client requests simultaneously. When a client tries to establish a connection with a server, the server socket accepts the connection and creates a separate socket (client socket) to communicate with the client. The server socket continues to listen for more incoming connections while the client socket handles the communication with the connected client.

(c)
What is Beans ? Explain its advantages in brief.
=)In Java, a bean is a reusable software component that follows specific naming conventions and design patterns. It is a class that encapsulates data and provides methods to manipulate and access that data. Beans are commonly used in Java development to create modular and reusable components that can be easily integrated into applications.

Advantages of Beans:

1. Reusability: Beans promote code reusability by encapsulating functionality in a self-contained module. They can be easily integrated into different applications without requiring significant modifications.

2. Modularity: Beans allow for modular development, where each component can be developed independently and then combined to build complex applications. This modular approach simplifies development, testing, and maintenance.

3. Ease of Integration: Beans provide a standardized interface, making it easier to integrate them into various frameworks and development environments. They can be seamlessly used in different Java technologies such as JavaBeans, Enterprise JavaBeans (EJB), Spring, etc.

4. Component-based Development: Beans enable component-based development, where different components can be combined to create larger systems. This promotes a modular and scalable approach to software development.

5. Bean Customization: Beans support customization through properties, which can be accessed and modified by other components. This allows for flexible configuration and adaptation of the bean's behavior without modifying its underlying code.

6. Support for Events: Beans can generate and consume events, allowing them to communicate and interact with other components. This event-driven model enables loose coupling and promotes better system design.

7. Tool Support: Beans benefit from extensive tooling support in Java development environments. Various IDEs provide visual editors and wizards to create, configure, and manipulate beans, making development faster and more efficient.

(d)
Write a Multithreading program in Java to display all the
alphabets from A to Z after 3 seconds.
=)
```java
public class AlphabetThread extends Thread {
    @Override
    public void run() {
        for (char c = 'A'; c <= 'Z'; c++) {
            System.out.println(c);

            try {
                Thread.sleep(3000); // Delay of 3 seconds
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
        }
    }

    public static void main(String[] args) {
        AlphabetThread alphabetThread = new AlphabetThread();
        alphabetThread.start();
    }
}

```
(e)
Explain JDBC Drivers with a suitable diagram.

=)https://www.javatpoint.com/jdbc-driver
Java Database Connectivity (JDBC) is an application programming interface (API) for the programming language Java, which defines how a client may access any kind of tabular data, especially relational database. It is part of Java Standard Edition platform, from Oracle Corporation. It acts as a middle layer interface between java applications and database.

The JDBC classes are contained in the Java Package java.sql and javax.sql.
JDBC helps you to write Java applications that manage these three programming activities:

Connect to a data source, like a database.
Send queries and update statements to the database
Retrieve and process the results received from the database in answer to your query

JDBC drivers are client-side adapters (installed on the client machine, not on the server) that convert requests from Java programs to a protocol that the DBMS can understand. There are 4 types of JDBC drivers:

Type-1 driver or JDBC-ODBC bridge driver
Type-2 driver or Native-API driver
Type-3 driver or Network Protocol driver
Type-4 driver or Thin driver
Type-1 driver

Type-1 driver or JDBC-ODBC bridge driver uses ODBC driver to connect to the database. The JDBC-ODBC bridge driver converts JDBC method calls into the ODBC function calls. Type-1 driver is also called Universal driver because it can be used to connect to any of the databases.

As a common driver is used in order to interact with different databases, the data transferred through this driver is not so secured.
The ODBC bridge driver is needed to be installed in individual client machines.
Type-1 driver isn’t written in java, that’s why it isn’t a portable driver.
This driver software is built-in with JDK so no need to install separately.
It is a database independent driver.
Type-2 driver

The Native API driver uses the client -side libraries of the database. This driver converts JDBC method calls into native calls of the database API. In order to interact with different database, this driver needs their local API, that’s why data transfer is much more secure as compared to type-1 driver.

Driver needs to be installed separately in individual client machines
The Vendor client library needs to be installed on client machine.
Type-2 driver isn’t written in java, that’s why it isn’t a portable driver
It is a database dependent driver.
Type-3 driver

The Network Protocol driver uses middleware (application server) that converts JDBC calls directly or indirectly into the vendor-specific database protocol. Here all the database connectivity drivers are present in a single server, hence no need of individual client-side installation.

Type-3 drivers are fully written in Java, hence they are portable drivers.
No client side library is required because of application server that can perform many tasks like auditing, load balancing, logging etc.
Network support is required on client machine.
Maintenance of Network Protocol driver becomes costly because it requires database-specific coding to be done in the middle tier.
Switch facility to switch over from one database to another database.
Type-4 driver

Type-4 driver is also called native protocol driver. This driver interact directly with database. It does not require any native database library, that is why it is also known as Thin Driver.

Does not require any native library and Middleware server, so no client-side or server-side installation.
It is fully written in Java language, hence they are portable drivers.
5.
Attempt any two :
[2×8=16]
(a)
Write a Socket program in Java to check whether given file
is present on server or not, If it is present then display its
content on the server’s machine otherwise display error message.
=)
```java
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.io.PrintWriter;
import java.net.Socket;

public class FileCheckerClient {
    public static void main(String[] args) {
        String serverAddress = "localhost";
        int serverPort = 1234;
        String filePath = "/path/to/file.txt";

        try {
            // Connect to the server
            Socket socket = new Socket(serverAddress, serverPort);
            
            // Create I/O streams for communication
            BufferedReader input = new BufferedReader(new InputStreamReader(socket.getInputStream()));
            PrintWriter output = new PrintWriter(socket.getOutputStream(), true);
            
            // Send the file path to the server
            output.println(filePath);
            
            // Receive the response from the server
            String response = input.readLine();
            
            // Check the response and display the result
            if (response.equals("FOUND")) {
                System.out.println("File found on the server. Contents:");
                String line;
                while ((line = input.readLine()) != null) {
                    System.out.println(line);
                }
            } else if (response.equals("NOT_FOUND")) {
                System.out.println("File not found on the server.");
            } else {
                System.out.println("Invalid response from the server.");
            }
            
            // Close the socket
            socket.close();
        } catch (IOException e) {
            System.out.println("An error occurred: " + e.getMessage());
        }
    }
}

```
Or
Write a Java program to accept file name from user, check
if it is available on server machine or not, if it is available
the display its contents on client machine otherwise display
the message ‘‘File Not Found’’.
=)
**Client Program:**

```java
import java.io.*;
import java.net.Socket;

public class FileClient {
    public static void main(String[] args) {
        String serverAddress = "localhost";
        int serverPort = 1234;

        try {
            // Connect to the server
            Socket socket = new Socket(serverAddress, serverPort);

            // Create I/O streams for communication
            BufferedReader input = new BufferedReader(new InputStreamReader(socket.getInputStream()));
            PrintWriter output = new PrintWriter(socket.getOutputStream(), true);

            // Accept the file name from the user
            BufferedReader userInput = new BufferedReader(new InputStreamReader(System.in));
            System.out.print("Enter file name: ");
            String fileName = userInput.readLine();

            // Send the file name to the server
            output.println(fileName);

            // Receive the response from the server
            String response = input.readLine();

            // Check the response and display the result
            if (response.equals("FOUND")) {
                System.out.println("File found on the server. Contents:");
                String line;
                while ((line = input.readLine()) != null) {
                    System.out.println(line);
                }
            } else if (response.equals("NOT_FOUND")) {
                System.out.println("File not found on the server.");
            } else {
                System.out.println("Invalid response from the server.");
            }

            // Close the socket
            socket.close();
        } catch (IOException e) {
            System.out.println("An error occurred: " + e.getMessage());
        }
    }
}
```

**Server Program:**

```java
import java.io.*;
import java.net.ServerSocket;
import java.net.Socket;

public class FileServer {
    public static void main(String[] args) {
        int serverPort = 1234;

        try {
            // Create a server socket
            ServerSocket serverSocket = new ServerSocket(serverPort);

            System.out.println("Server listening on port " + serverPort);

            while (true) {
                // Accept client connection
                Socket clientSocket = serverSocket.accept();

                // Create I/O streams for communication
                BufferedReader input = new BufferedReader(new InputStreamReader(clientSocket.getInputStream()));
                PrintWriter output = new PrintWriter(clientSocket.getOutputStream(), true);

                // Read the file name from the client
                String fileName = input.readLine();

                // Check if the file exists
                File file = new File(fileName);
                if (file.exists() && file.isFile()) {
                    // File found, send "FOUND" response
                    output.println("FOUND");

                    // Read and send the file content to the client
                    BufferedReader fileReader = new BufferedReader(new FileReader(file));
                    String line;
                    while ((line = fileReader.readLine()) != null) {
                        output.println(line);
                    }
                    fileReader.close();
                } else {
                    // File not found, send "NOT_FOUND" response
                    output.println("NOT_FOUND");
                }

                // Close the client socket
                clientSocket.close();
            }
        } catch (IOException e) {
            System.out.println("An error occurred: " + e.getMessage());
        }
    }
}
```
(b)
Write a JSP script to check whether given mail ID is valid
or not. (Mail ID should contain one @ symbol and at least
one Dot(.) symbol).
=)
```jsp
<%@ page language="java" %>
<%@ page import="java.util.regex.Pattern" %>

<!DOCTYPE html>
<html>
<head>
    <title>Email Validation</title>
</head>
<body>
    <h2>Email Validation</h2>

    <form method="post">
        <label for="email">Enter Email ID:</label>
        <input type="text" id="email" name="email" required>
        <button type="submit">Check</button>
    </form>

    <%-- JSP Scriptlet --%>
    <% 
        // Get the email ID submitted by the user
        String email = request.getParameter("email");

        // Define the email pattern
        String emailPattern = "^[A-Za-z0-9+_.-]+@[A-Za-z0-9.-]+$";

        // Check if the email matches the pattern
        boolean isValidEmail = Pattern.matches(emailPattern, email);
    %>

    <%-- Display the result --%>
    <% if (email != null && !email.isEmpty()) { %>
        <% if (isValidEmail) { %>
            <p><strong><%= email %></strong> is a valid email ID.</p>
        <% } else { %>
            <p><strong><%= email %></strong> is not a valid email ID.</p>
        <% } %>
    <% } %>
</body>
</html>

```
Or
Write a Servlet program to display the details of employee
in tabular format. Employee table structure (eno, ename, sal,
design)
=)
```java
import java.io.*;
import javax.servlet.*;
import javax.servlet.http.*;
import java.util.*;

public class EmployeeDetailsServlet extends HttpServlet {
    public void doGet(HttpServletRequest request, HttpServletResponse response)
            throws ServletException, IOException {
        // Create a list of employees
        List<Employee> employeeList = new ArrayList<>();
        employeeList.add(new Employee(1, "John Doe", 5000, "Manager"));
        employeeList.add(new Employee(2, "Jane Smith", 4000, "Developer"));
        employeeList.add(new Employee(3, "Mike Johnson", 6000, "Analyst"));
        employeeList.add(new Employee(4, "Sarah Williams", 4500, "Designer"));

        // Set the content type of the response
        response.setContentType("text/html");

        // Get the PrintWriter object
        PrintWriter out = response.getWriter();

        // Generate the HTML response
        out.println("<html>");
        out.println("<head><title>Employee Details</title></head>");
        out.println("<body>");
        out.println("<h2>Employee Details</h2>");
        out.println("<table border='1'>");
        out.println("<tr><th>Employee Number</th><th>Employee Name</th><th>Salary</th><th>Designation</th></tr>");

        // Loop through the employee list and generate table rows
        for (Employee employee : employeeList) {
            out.println("<tr>");
            out.println("<td>" + employee.getEno() + "</td>");
            out.println("<td>" + employee.getEname() + "</td>");
            out.println("<td>" + employee.getSal() + "</td>");
            out.println("<td>" + employee.getDesign() + "</td>");
            out.println("</tr>");
        }

        out.println("</table>");
        out.println("</body></html>");

        // Close the PrintWriter
        out.close();
    }
}

class Employee {
    private int eno;
    private String ename;
    private double sal;
    private String design;

    public Employee(int eno, String ename, double sal, String design) {
        this.eno = eno;
        this.ename = ename;
        this.sal = sal;
        this.design = design;
    }

    public int getEno() {
        return eno;
    }

    public String getEname() {
        return ename;
    }

    public double getSal() {
        return sal;
    }

    public String getDesign() {
        return design;
    }
}
```
