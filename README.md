# ⚡️Clean Architecture | overview
![](https://raw.githubusercontent.com/iuno-san/Clean-Architecture/main/Clean-architecture.png) <br>
The Clean Architecture design pattern is a great choice to build scalable, maintainable, and tested applications. Clean Architecture is based on the principle of separating dependencies between different layers of the application, which allows for easy modifications and replacement of individual elements without affecting the entire system.
<br><br>
Below are the steps that can help you build ASP.NET Core MVC applications using the Clean Architecture pattern: <br><br>

# 🔥 Application layers
## Clean Architecture divides an application into several layers, typically these are:
- <code>Presentation Layer</code>: Responsible for handling user interaction and displaying data. In ASP.NET Core MVC, this would be the Controllers and Views layer. <br><br>
- <code>Application Layer</code>: Responsible for application logic and data processing. This is where the application services that contain business operations are located. <br><br>
- <code>Domain Layer</code>: Contains business logic and entities that represent application domain objects. <br><br>
- <code>Infrastructure Layer</code>: Responsible for technical aspects of the application, such as access to the database, external services, repository implementations, etc.
<br><br>

# ⭐️ Project Creation
In ASP.NET Core, create a new project by selecting the "ASP.NET Core Web Application" template and specifying "<code>MVC</code>" as the project type.
<br><br>

# 🏋️‍♀️ Project organization
Make sure your project is properly organized to separate different layers and avoid strong dependencies between them. For example, you can create separate folders for each layer.
<br><br>

# 🌌 Implementation of layers
- <code>Domain layer</code>: In this layer, define entities that represent the main objects in your domain. Avoid dependencies on other layers here. <br><br>
- <code>Application layer</code>: Here create application services that will contain the logic of business operations. These services will use entities from the domain layer. Make sure that the application layer has no dependencies on the presentation or infrastructure layer. <br><br>
- <code>Presentation layer</code>: This layer contains controllers and views. Controllers will use application services to handle user requests and process data. Try to minimize logic in controllers and move it to the application layer. <br><br>
- <code>Infrastructure layer</code>: here implement specific mechanisms for database access, external services or other technical aspects of the application. You can use the repository pattern to separate data access from the rest of the application.
<br><br>

# ⛓ Dependencies
Make sure that the dependencies between layers are properly configured. Typically, the presentation layer and the application layer will have dependencies on the domain layer, and the infrastructure layer on the others. Avoid dependencies on the presentation or infrastructure layers in the domain layer.
<br><br>

# ⚙️ Testing
Taking care of unit testing of code is key in Clean Architecture. You can use unit testing tools such as <code>xUnit</code>, <code>NUnit</code> or <code>MSTest</code> to test individual units of code in isolation.
<br><br>

# 🤖 Configuration
Configure Dependency Injection <code>(DI)</code> mechanisms in ASP.NET Core to provide appropriate service implementations between layers.
<br><br>

# 🎥 Monitoring
Consider adding monitoring and logging mechanisms to easily detect problems in the application.
Development and maintenance:
Once the basic architecture is complete, you can continue to develop the application by adding new features and improving existing ones.
<br><br>

# 🍂 Summary
Keep in mind that the Clean Architecture pattern may require more effort in the beginning, but provides many benefits in the long run, especially if the application grows and becomes more complex. With properly organized code and isolated layers, maintaining the application and making changes is much easier.
