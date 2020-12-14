## **Difference between string and symbol in ruby?**
Strings are any text written between quotation marks, while a symbol is any text that begins with a colon. But strings and symbols have different functionality that make them useful for different purposes in programming. Significant difference between strings and symbols is how they are stored in memory.

Every time a string is written, it creates a new object with a new place in memory, even if the string is textually identical to an existing string. However, since symbols are immutable, they always refer to the same object and the same place in memory.

## **CLI command to read first 10 lines?**
We can use `head` command to read first n lines.  
```
head filepath
```  
By default, head shows first 5 lines. We can specify the number of lines using `-n`.  
```
head -n 10 filepath
# or
head -10 filepath
```
## **What is Ancestor Chaining in Ruby?**
Ancestor chaining is the way the interpreter copes with method invocations within the class hierarchy. When we invoke a method, Ruby looks for it in the current class or module. If it is not found in the current class or module, Ruby looks for it in the next class/module. This forms an ancestor chain. To see the ancestor chain of any class we can call `ancestors` on that class.
```
String.ancestors
```

## **Difference between *delete* and *destroy* in rails?**

Delete deletes the row with the primary key matching the id argument, using SQL DELETE statement, and returns the number of rows deleted. Active record objects are not instantiated, so the object's call backs are not executed.  
```
Todo.delete(id)
```
Destroy destroys an object that has the given id. The object is instantiated first, therefore all callbacks and filters are fired off before the object is deleted.

```
Todo.destroy(id)
```

## ***break* and *continue* in Javascript**
Break statement mainly used to terminate the loop.  
```
for (let num = 0; num < 10; num++) {
    if (num == 5) {
        break;
    } else {
        console.log(num);
    }
}
// OUTPUT
// 0 1 2 3 4
```
In the above example, the control comes out of the loop when `num` is equals to `5`.

Continue statement is used to skip the current iteration and executes the next iteration.  
```
for (let num = 0; num < 10; num++) {
    if (num == 5) {
        continue;
    } else {
        console.log(num)
    }
}
// OUTPUT
// 0 1 2 3 4 6 7 8 9
```
In the above example, the control skips the iteration when `num` is equal to `5` and moves to next iteration.

## **What is *opacity* in CSS?**
Opacity property sets the opacity level for an element.
Opacity level describes the transparency-level, where 1 is not transparent. 0 is completely transparent.
```
div {
    background-color: red;
    opacity: 0.2; //20% transparency
}
```

## **How to declare constants in Ruby?**
In Ruby, Constants always starts with capital letter. Constants are defined outside of methods.  
Constants are used for value that are not supposed to change.  
```
# VALID CONSTANTS
ABC = 1
Foo = 3
```  
We can access the constants outside the class using `::`.
```
Math::PI
```

## **What is CRON job? What is the command for modifying CRON?**
CRON job is a LINUX command used for scheduling tasks to be executed sometime in the future.  
We can modify the CRON jobs using the following command.  
```
crontab -e
```

##  **Cursor concept in SQL?**
Cursor is a read-only pointer to a fully executed SELECT statement's result set. Cursors are typically used within applications that maintain a persistent connection to the database. By executing the cursor and maintaining a reference to its returned result set, an application can more efficiently manage which row to retrieve from a result set at different times, without having to re-execute the query with different LIMIT and OFFSET clause.