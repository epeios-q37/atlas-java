# *Java* version of the *Atlas* toolkit

[![Run on Repl.it](https://q37.info/s/kpm7xhfm.png)](https://q37.info/s/3vwk3h3n)  [![About online demonstrations](https://img.shields.io/badge/about-online%20demonstrations-informational)](https://q37.info/s/sssznrb4)

[![Version 0.13](https://img.shields.io/static/v1.svg?&color=90b4ed&label=Version&message=0.13&style=for-the-badge)](http://github.com/epeios-q37/atlas-java/)
[![license: MIT](https://img.shields.io/github/license/epeios-q37/atlas-java?color=yellow&style=for-the-badge)](https://github.com/epeios-q37/atlas-java/blob/master/LICENSE)
[![Documentation](https://img.shields.io/static/v1?label=documentation&message=atlastk.org&color=ff69b4&style=for-the-badge)](https://atlastk.org)  



<!--
Si la table ci-dessous est modifiée, alors modifier également (pages du site atlastk.org) :
- la page 'Home' ;
- la page 'Online demonstrations' ;
-->

> The [*Atlas* toolkit](https://atlastk.org) is available for:
> | &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | Language | Online demonstrations | Repo. #1 | #2 | #3 |Stars
> |-|-|:-:|:-:|:-:|:-:|:-:|
> | ![Java](https://q37.info/s/sgb9nq7x.svg) | [*Java*](https://q37.info/s/qtnkp9w4)  | [![Run on Replit](https://q37.info/s/kpm7xhfm.png)](https://q37.info/s/3vwk3h3n) | [*Framagit*](https://framagit.org/epeios-q37/atlas-java) | [*GitHub*](https://github.com/epeios-q37/atlas-java) | [*GitLab*](https://gitlab.com/epeios-q37/atlas-java) | [![Stars for atlas-java](https://img.shields.io/github/stars/epeios-q37/atlas-java.svg?label=)](https://github.com/epeios-q37/atlas-java/stargazers)
> | ![Node.js](https://q37.info/s/b9ctj4bb.svg) | [*Node.js*](https://q37.info/s/3d7hr733) | [![Run on Replit](https://q37.info/s/kpm7xhfm.png)](https://q37.info/s/st7gccd4) | [*Framagit*](https://framagit.org/epeios-q37/atlas-node) | [*GitHub*](https://github.com/epeios-q37/atlas-node) | [*GitLab*](https://gitlab.com/epeios-q37/atlas-node) | [![Stars for atlas-node](https://img.shields.io/github/stars/epeios-q37/atlas-node.svg?label=)](https://github.com/epeios-q37/atlas-node/stargazers)
> | ![Perl](https://q37.info/s/v9qkzvhk.svg) | [*Perl*](https://q37.info/s/4nvmwjgg)  | [![Run on Replit](https://q37.info/s/kpm7xhfm.png)](https://q37.info/s/h3h34zgq) | [*Framagit*](https://framagit.org/epeios-q37/atlas-perl) | [*GitHub*](https://github.com/epeios-q37/atlas-perl) | [*GitLab*](https://gitlab.com/epeios-q37/atlas-perl) | [![Stars for atlas-perl](https://img.shields.io/github/stars/epeios-q37/atlas-perl.svg?label=)](https://github.com/epeios-q37/atlas-perl/stargazers)
> | ![Python](https://q37.info/s/t4s3p4rk.svg) | [*Python*](https://q37.info/s/pd7j9k4r)  | [![Run on Replit](https://q37.info/s/kpm7xhfm.png)](https://q37.info/s/vwpsw73v) | [*Framagit*](https://framagit.org/epeios-q37/atlas-python) | [*GitHub*](https://github.com/epeios-q37/atlas-python)  | [*GitLab*](https://gitlab.com/epeios-q37/atlas-python) | [![Stars](https://img.shields.io/github/stars/epeios-q37/atlas-python.svg?label=)](https://github.com/epeios-q37/atlas-python/stargazers)
> | ![Ruby](https://q37.info/s/ngxztq4t.svg) | [*Ruby*](https://q37.info/s/gkfj3zpz)  | [![Run on Replit](https://q37.info/s/kpm7xhfm.png)](https://q37.info/s/9thdtmjg) | [*Framagit*](https://framagit.org/epeios-q37/atlas-ruby) | [*GitHub*](https://github.com/epeios-q37/atlas-ruby) | [*GitLab*](https://gitlab.com/epeios-q37/atlas-ruby) | [![Stars for atlas-ruby](https://img.shields.io/github/stars/epeios-q37/atlas-ruby.svg?label=)](https://github.com/epeios-q37/atlas-ruby/stargazers)



---

## A GUI with *Java* in a couple of minutes

Click the animation to see a screencast of programming this ["Hello, World!" program](https://en.wikipedia.org/wiki/%22Hello,_World!%22_program) with *Java* in a matter of minutes:

[![Building a GUI in with *Java* in less then 10 minutes](https://q37.info/s/qp4z37pg.gif)](https://q37.info/s/vd9xz7jp)

Same video on [*Peertube*](https://en.wikipedia.org/wiki/PeerTube): <https://q37.info/s/qs4dx4rm>.

Source code:

```java
import info.q37.atlas.*;

class Hello extends Atlas {
 private static String BODY =
  "<fieldset>" +
  " <input id=\"Input\" xdh:onevent=\"Submit\" value=\"World\"/>" +
  " <button xdh:onevent=\"Submit\">Hello</button>" +
  " <hr/>" +
  " <fieldset>" +
  "  <output id=\"Output\">Greetings displayed here!</output>" +
  " </fieldset>" +
  "</fieldset>";

  @Override
  public void handle(String action, String id)
  {
    switch(action) {
    case "":
      dom.inner("", BODY);
      break;
    case "Submit":
      String name = dom.getValue("Input");
      dom.begin("Output", "<div>Hello, " + name + "!</div>");
      dom.setValue("Input", "" );
      break;
    }
    dom.focus("Input");
  }

  public static void main(String[] args)
  {
    launch(() -> new Hello());
  }
}
```

### See for yourself right now - it's quick and easy!

#### Online, with nothing to install

To run above "Hello, World!" program directly in your browser, as seen in corresponding video, follow this link: <https://replit.com/@AtlasTK/hello-java>.

Thanks to [*Replit*](https://q37.info/s/mxmgq3qm), an [online IDE](https://q37.info/s/zzkzbdw7), you can write and run programs using the *Atlas* toolkit directly in your web browser, without having to install *Java* on your computer [![About online demonstrations](https://img.shields.io/badge/about-online%20demonstrations-informational)](https://q37.info/s/sssznrb4).

To see more examples, like the following [*TodoMVC*](http://todomvc.com/), simply:
- go [here](https://q37.info/s/3vwk3h3n) (also accessible with the [![Run on Repl.it](https://q37.info/s/kpm7xhfm.png)](https://q37.info/s/3vwk3h3n) button at the top of this page),
- click on the green `run` button,
- choose the demonstration to launch,
- open the then displayed URL in a browser (should be clickable), 
- … and, as you wish, run your own tests directly in your browser, by modifying the code of the examples or by writing your own code.

[![TodoMVC](https://q37.info/download/TodoMVC.gif "The TodoMVC application made with the Atlas toolkit")](https://q37.info/s/3vwk3h3n)

#### With *Java* on your computer

- on *Windows* (pay attention to the `;` on last line):
```bash
# You can replace 'github.com' with 'framagit.org'.
# DON'T copy/paste this and above line!
git clone https://github.com/epeios-q37/atlas-java
cd atlas-java/examples/Hello
java -cp .;../../Atlas.jar Hello
```

- on other platforms (pay attention to the `:` on last line):
```bat
REM You can replace 'github.com' with 'framagit.org'.
REM DON'T copy/paste this and above line!
git clone https://github.com/epeios-q37/atlas-java
cd atlas-java/examples/Hello
java -cp .:../../Atlas.jar Hello
```



## Your turn

If you want to take your code to the next level, from [CLI](https://q37.info/s/cnh9nrw9) to [GUI](https://q37.info/s/hw9n3pjs), then you found the right toolkit.

With the [*Atlas* toolkit](http://atlastk.org/), you transform your programs in modern web applications ([*SPA*](https://q37.info/s/7sbmxd3j)) without the usual hassles:
- no *JavaScript* to write; only *HTML*(/*CSS*) and *Java*,
- no [front and back end architecture](https://q37.info/s/px7hhztd) to bother with,
- no [web server](https://q37.info/s/n3hpwsht) (*Apache*, *Nginx*…) to install,
- no need to deploy your application on a remote server,
- no incoming port to open on your internet box or routeur.

The *Atlas* toolkit is written in pure *Java*, with no native code and no dependencies, allowing the *Atlas* toolkit to be used on all environments where *Java* is available. 

And simply by running them on a local computer connected to internet, applications using the *Atlas* toolkit will be accessible from the entire internet on laptops, smartphones, tablets…

## Content of the repository

The `atlastk` directory contains the *Java* source code of the *Atlas* toolkit.

`Atlas.jar` is the file you have to reference in the [*classpath*](https://en.wikipedia.org/wiki/Classpath_(Java)) in order to use the *Atlas* toolkit in your own program.

The `examples` directory contains some examples.

To run an example, go inside its directory (`Blank`, `Chatroom`…) and launch:

- under *Windows*: `java -cp .;../../Atlas.jar <Name>` (with semi-colon as *classpath* separator),
- under other platforms: `java -cp .:../../Atlas.jar <Name>` (with colon as *classpath* separator).

where `<Name>` is the name of the example (`Blank`, `Chatroom`…).
