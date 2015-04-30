# Introduction #

The User Agent Parser library is a commercial-friendly Java library for parsing the User-Agent header that browsers send along with their web requests. You can use it to determine the browser type and version, along with the underlying operating system the browser is running on.

It's based on a [great writeup](http://www.texsoft.it/index.php?c=software&m=sw.php.useragent&l=it) on the textSoft site.


# Usage #

Here's the basic usage in the form of a JUnit test:

```
    String header = "Mozilla/5.0 (iPhone; U; CPU iPhone OS 3_1_3 like Mac OS X; en-us) " +
                        "AppleWebKit/528.18 (KHTML, like Gecko) Version/4.0 Mobile/7E18 Safari/528.16";
    UserAgentParser uap = new UserAgentParser(header);
    assertEquals("iPhone", uap.getBrowserOperatingSystem());
    assertEquals("Safari", uap.getBrowserName());
    assertEquals("528.16", uap.getBrowserVersion());
```

# Building from Source #

The project builds with Maven on any JDK 5+ machine. Clone the project, then change into the root directory and issue a:

```
    mvn clean package
```

And you'll have a binary in the /target/ subdirectory.

# License #

The library is licensed under an Apache 2 license. You are free to use it in commercial products or modify it in any way you see fit. Knock yourself out.