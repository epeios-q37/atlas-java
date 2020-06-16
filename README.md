# *Java* version of the *Atlas* toolkit

![For Java](https://q37.info/download/assets/Java.png "Java logo")

[![Run on Repl.it](https://repl.it/badge/github/epeios-q37/atlas-java)](https://q37.info/s/3vwk3h3n)
[![Version 0.11](https://img.shields.io/static/v1.svg?&color=90b4ed&label=Version&message=0.11)](http://github.com/epeios-q37/atlas-java/)
[![Stars](https://img.shields.io/github/stars/epeios-q37/atlas-java.svg?style=social)](https://github.com/epeios-q37/atlas-java/stargazers)
[![license: MIT](https://img.shields.io/github/license/epeios-q37/atlas-java?color=yellow)](https://github.com/epeios-q37/atlas-java/blob/master/LICENSE)
[![Homepage](https://img.shields.io/static/v1?label=homepage&message=atlastk.org&color=ff69b4)](https://atlastk.org)




> *This toolkit is available for:*
> - *Java*: <http://github.com/epeios-q37/atlas-java>
> - *Node.js*: <http://github.com/epeios-q37/atlas-node>
> - *Perl*: <http://github.com/epeios-q37/atlas-perl>
> - *Python*: <http://github.com/epeios-q37/atlas-python>
> - *Ruby*: <http://github.com/epeios-q37/atlas-ruby>



---

## Straight to the point: the [*Hello, World!*](https://en.wikipedia.org/wiki/%22Hello,_World!%22_program) program

### Source code

```java
import info.q37.atlas.*;

class Hello extends Atlas {

 private static String body =
  "<div style=\"display: table; margin: 50px auto auto auto;\">" +
  " <fieldset>" +
  "   <input id=\"input\" maxlength=\"20\" placeholder=\"Enter a name here\"'" +
  "          type=\"text\" data-xdh-onevent=\"Submit\"/>" +
  "   <div style=\"display: flex; justify-content: space-around; margin: 5px auto auto auto;\">" +
  "    <button data-xdh-onevent=\"Submit\">Submit</button>" +
  "    <button data-xdh-onevent=\"Clear\">Clear</button>" +
  "  </div>" +
  " </fieldset>" +
  "</div>";

 @Override
 public void handle(String action, String id)
 {
  switch(action) {
  case "": // Action label corresponding to a new session.
   dom.setLayout("", body);
   break;
  case "Submit":
   dom.alert("Hello, " + dom.getContent("input") + "!" );
   break;
  case "Clear":
   if ( dom.confirm("Are you sure ?") )
    dom.setContent("input", "");
   break;
  }

  dom.focus("input");
 }

 public static void main(String[] args)
 {
  launch(() -> new Hello());
 }
}
```

### Result

[![Little demonstration](https://q37.info/download/assets/Hello.gif "A basic example")](https://q37.info/s/3vwk3h3n)

### Try it yourself now

#### Online, with nothing to install

Thanks to [Replit](https://q37.info/s/mxmgq3qm), an [online IDE](https://q37.info/s/zzkzbdw7), you can write and run programs using the *Atlas* toolkit directly in your web browser, without having to install *Java* on your computer.

To see some examples, like the following [*TodoMVC*](http://todomvc.com/) application or the above [*Hello, World!*](https://en.wikipedia.org/wiki/%22Hello,_World!%22_program) program, simply:
-  go [here](https://q37.info/s/3vwk3h3n) (or click on the [![Run on Repl.it](https://repl.it/badge/github/epeios-q37/atlas-java)](https://q37.info/s/3vwk3h3n) badge at the top of this page),
-  click on the green `run` button,
-  select the demonstration you want to see,
-  click (or scan with your smartphone) the then displayed [QR code](https://q37.info/s/3pktvrj7).

[![TodoMVC](https://q37.info/download/TodoMVC.gif "The TodoMVC application made with the Atlas toolkit")](https://q37.info/s/3vwk3h3n)

#### With *Java* on your computer

- on *Windows* (pay attention to the `;` on last line):
```
git clone https://github.com/epeios-q37/atlas-java
cd atlas-java/examples/Hello
java -cp .;../../Atlas.jar Hello
```

- on other platforms (pay attention to the `:` on last line):
```
git clone https://github.com/epeios-q37/atlas-java
cd atlas-java/examples/Hello
java -cp .:../../Atlas.jar Hello
```

## Your turn

If you want to:

- take your code to the next level, from [CLI](https://q37.info/s/cnh9nrw9) to [GUI](https://q37.info/s/hw9n3pjs),
- teach your students to program a GUI, 
- impress your teacher with a blowing GUI,
- easily share your programs with all you family and friends,

then you found the right toolkit.

With the [*Atlas* toolkit](http://atlastk.org/), writing modern web applications ([*SPA*](https://q37.info/s/7sbmxd3j)) has never been this easy:
- no *JavaScript* to write; only *HTML* and *Java*,
- no [front and back end architecture](https://q37.info/s/px7hhztd) to bother with,
- no [web server](https://q37.info/s/n3hpwsht) (*Apache*, *Nginx*…) to install,
- no need to deploy your application on a remote server,
- no incoming port to open on your internet box.

The *Atlas* toolkit is written in pure *Java*, with no native code and no dependencies, allowing the *Atlas* toolkit to be used on all environments where *Java* is available. 

Simply by running them on a local computer with a simple internet connexion, applications using the *Atlas* toolkit will be accessible from the entire internet on laptops, smartphones, tablets…

## Content of the repository

The `atlastk` directory contains the *Java* source code of the *Atlas* toolkit.

`Atlas.jar` is the file you have to reference in the [*classpath*](https://en.wikipedia.org/wiki/Classpath_(Java)) in order to use the *Atlas* toolkit in your own program.

The `examples` directory contains some examples.

To run an example, go inside its directory (`Blank`, `Chatroom`…) and launch:

- under *Windows*: `java -cp .;../../Atlas.jar <Name>` (with semi-colon as *classpath* separator),
- under other platforms: `java -cp .:../../Atlas.jar <Name>` (with colon as *classpath* separator).

where `<Name>` is the name of the example (`Blank`, `Chatroom`…).