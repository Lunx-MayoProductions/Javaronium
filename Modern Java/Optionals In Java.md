# Optionals

## So what will we do here today`?

We will start using the `Optional<T>` Object in Java.

### Your Advantes and downsides

Advanteges:
 - NullSafe Object
 - API Compability
 - Easy use

Downside:
 - Users can get null values if not used correct
 - Not every API is updated.
 - Sometimes new Users dont understand why to use it.

### Lets start coding
Imagine you are at work (or school) and want to represent a **mate** as an **Object in Java**, but you dont know if hes **sick or not**. So the **value mabye null**.
To fix this problem, we got Optionals so let me straight up show it!

```java
public Optional<String> getMatesName(Optional<Mate> mate){
    if (mate.isPresent(){
        return mate.get().toString();
    }else{
        return "SICK";
    }
}

```

Lets break it down! So we created a method to get a mates name that returns an `Optional<String>` and we pass in a `Optional<Mate>` but the mate inside the optional might be null!
So we check that with `xyz.isPresent()`. If he is not null itl return true, else false. Thats how we can check it!
Now to get the actual Object (and we are sure its not null) we do `xyz.get()` thats how we get him.
Not to simple but understandable!