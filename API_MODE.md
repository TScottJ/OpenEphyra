==============================
Using OpenEphyra in "API mode"
==============================

Normally, OpenEphyra is run as a standalone program, by executing one of the
script files. However, the various classes and methods can also be called
from another Java application.

This doc describes how you can use OpenEphyra from a Java archive (.JAR) and
call its search functions programatically. This example is taken from a demo
that was done using ProgramD, and shows how to pass a question to the
OpenEphyra QA system and retrieve the resulting answer.

The basic steps are:
1. Build the OpenEphyra project, then export it to a Java archive (JAR) file.
2. Add the JAR file to your host application's Java build path (libraries).
3. Add import statements to your .java file for importing both the OpenEphyra
main class and the Result class.
4. Instantiate the OpenEphyra main class. This should only be done once, since
a lot of initialization takes place during construction of OpenEphyra.
5. Call the askFactoid() method of OpenEphyra. This returns a Result object
containing the answer and confidence score.

Example:
--------

```java
import info.ephyra.OpenEphyra;
import info.ephyra.search.Result;

public class Foo
{
    protected OpenEphyra openEphyra = null;

    public Foo()
    {
        // Instantiate and initialize the main OpenEphyra object. The string
        // parameter is the path to the OpenEphyra root folder, where the RES
        // and CONF subfolders can be found (empty string for common root).
        this.openEphyra = new OpenEphyra("");
    }

    public String getAnswer(String question)
    {
        // Get answer from OpenEphyra:
        String oepAnswer = "";
        double oepScore = 0.0;
        Result oepResult = this.openEphyra.askFactoid(input);
        if (oepResult != null)
        {
            oepAnswer = oepResult.getAnswer();
            oepScore = oepResult.getScore();
            System.err.println("OpenEphyra Answer: " + oepAnswer +
                "\n    Score: " + Double.toString(oepScore));
        }

        return oepAnswer;
    }
}
```
