# The main things...

## Libaries

For this we are going to use JavaCord, if you want a tutorial on D4J or else, contact me!
:::info
JavaCord is often used, so support is easy to find.
:::
Also we are going to use Log4J (Log for Java)

## The Coding!

We are going to use gradle. Just because its better. So if you have not already, create a Project (I use IntelliJ Idea) with gradle as a building tool.
:::danger
You can but should not use maven
:::

### Gradle
```
repositories { mavenCentral() }
dependencies { implementation 'org.javacord:javacord:3.8.0' }
dependencies { runtimeOnly 'org.apache.logging.log4j:log4j-core:2.17.0' }
```

### Gradle KTS

```
repositories {
maven(
    "https://oss.sonatype.org/content/repositories/snapshots/"
)
}
dependencies {
    implementation "org.javacord:javacord:3.9.0-SNAPSHOT"
    runtimeOnly 'org.apache.logging.log4j:log4j-core:2.17.0'
}
```

## What you need
You should already have a (discord application.)[https://discordapp.com/developers/applications/me] and have the token reset & copied.

## Actual Coding this time.

**First** create your main class (exmpl: `Main.java`)
Then we are just going to log into the bot using:
```
String TOKEN = ...;
DiscordApi api = new DiscordApiBuilder()
        .setToken(TOKEN)
        .setAllNonPrivilegedIntents()
        .login().join();
```

So what did we do here? We first created a String with the bots token.
After that we created a new instance of `DiscordApi` with `new DiscordApiBuilder()` and we set the parameters. 
Because it returns a CompleteAbleFuture we used `.join()` to recive the object.