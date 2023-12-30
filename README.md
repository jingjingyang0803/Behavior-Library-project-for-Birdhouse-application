# behavior library Project

This is the Behavior Library project for our Birdhouse application. This library defines the behaviors that our birds can have.

## Getting Started

To use this library, clone the project to your local machine.

```bash
git clone https://github.com/jingjingyang0803/Behavior-Library-project-for-Birdhouse-application.git
```

## Project Structure

The project includes the following main components:

- `FlyBehavior.java`: This is the interface that represents flying behavior.
- `QuackBehavior.java`: This is the interface that represents quacking behavior.
- Implementations of `FlyBehavior` and `QuackBehavior`: These classes define specific ways a bird can fly and quack.

  The classes `FlyNoWay`, `FlyRocketPowered`, and `FlyWithWings` are concrete implementations of the `FlyBehavior` interface, meaning they define specific ways a bird can fly.

  Similarly, `MuteQuack`, `Quack`, and `Squeak` are concrete implementations of the `QuackBehavior` interface, providing specific ways a bird can quack.

The project follows the Strategy design pattern. This pattern allows the bird's behavior to change at runtime.

## Using the Library

To add a library as a dependency in your Maven configuration file (pom.xml), follow these steps:

1. Open your pom.xml file.
2. Find the `<dependencies>` section. If it doesn't exist, you can create it.
3. Add a `<dependency>` element inside the `<dependencies>` section with the group ID, artifact ID, and version of this behavior library:

```xml
<dependencies>
  <dependency>
    <groupId>com.example.lib</groupId>
    <artifactId>behavior-library</artifactId>
    <version>1.0-SNAPSHOT</version>
  </dependency>
</dependencies>

```

4. Save your pom.xml file.
5. Maven should automatically download and link the library next time you build your project.
6. You can use this library in your bird classes by including instances of `FlyBehavior` and `QuackBehavior` and calling their methods when needed.

## Installation

Once you've made any necessary modifications, you can install the library using Maven:

```bash
cd <your-project-directory>
mvn install
```

This will install the library to your local Maven repository, making it available for other projects on your machine to use as a dependency.
