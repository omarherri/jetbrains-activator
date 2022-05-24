# JetBrains License Server Activator 2.0 🔓

1. Close application
2. Add `jetbrains.jar` file anywhere you like
3. Add VM Options
4. Open application
5. Add License server, choose from [license_servers.txt](https://github.com/george-martinec/jetbrains-activator/blob/master/license_servers.txt), e.g.: `http://153.106.195.23:8080` and press activate

## VM Options

Add into file `phpstorm64.vmoptions` or `phpstorm64.exe.vmoptions` <br>
Or you can create free trial account and add it via application (Help > Edit Custom VM Options...)

```
-XX:ReservedCodeCacheSize=512m
-XX:+IgnoreUnrecognizedVMOptions
-XX:+UseG1GC
-XX:SoftRefLRUPolicyMSPerMB=50
-XX:CICompilerCount=2
-XX:+HeapDumpOnOutOfMemoryError
-XX:-OmitStackTraceInFastThrow
-ea
-Dsun.io.useCanonCaches=false
-Djdk.http.auth.tunneling.disabledSchemes=""
-Djdk.attach.allowAttachSelf=true
-Djdk.module.illegalAccess.silent=true
-Dkotlinx.coroutines.debug=off
-XX:ErrorFile=$USER_HOME/java_error_in_idea_%p.log
-XX:HeapDumpPath=$USER_HOME/java_error_in_idea.hprof

--add-opens=java.base/jdk.internal.org.objectweb.asm=ALL-UNNAMED
--add-opens=java.base/jdk.internal.org.objectweb.asm.tree=ALL-UNNAMED

-javaagent:/path/to/jetbrains.jar=jetbrains
```

#### Don't forget to change `/path/to/` to your actual path of the `jetbrains.jar` file !


### Works nicely with any plugins, e.g.: https://plugins.jetbrains.com/plugin/8006-material-theme-ui

## Operating System
| OS                                            | Supported Versions                  |
|-----------------------------------------------|-------------------------------------|
| [Ubuntu](https://ubuntu.com/download/desktop) | `Ubuntu 20.04.3 LTS` `Ubuntu 21.10` `Ubuntu 22.04 LTS` |
| [ZorinOS](https://zorin.com/)                 | `ZorinOS 15.3` `ZorinOS 16`         |
| [Windows](https://www.microsoft.com/windows)  | `Windows 10` `Windows 11`           |

There are a lots of Operating systems that I haven't tried, feel free to test and let me know.

<br>

| IDEs | Supported Versions |
| ------------- | ------------- |
|  <img align="center" src='https://raw.githubusercontent.com/george-martinec/jetbrains-evaluation-reset/master/icons/phpstorm_32x32.svg'/> | `2022.1`

There are a lots of IDEs that I haven't tried, feel free to test and let me know.

<br>

Made with ❤️ by [George Martinec](https://github.com/George-Martinec)
