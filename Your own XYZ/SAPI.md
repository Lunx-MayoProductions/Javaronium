# A Simple API

## Choose something to write an API for
**So we are going to assume we are writing a database API (neutral)**

## Making a main interface
Starting the API we are going to use an empty java project. Create an Interface and call it whatever you want, but put an s in front of it. (exmpl: SDataBaseAPI.java)

## You will now add your methods!

I would add methods like `class#start()` or things like that. But you have freedom so do what you want to do!

## Examples:

```java
public interface SDatabaseAPI{
    public void init();
    public void start(SDataBaseConfig config);
    public SDatabaseConnection connect(SConnectionConfig config);
}

public class Main implements SDatabaseAPI{
    public static void main(String[] args){
        ...
    }

    @Override
    ...
}