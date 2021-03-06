# npm-maven-plugin
Fetch [npm](https://npmjs.org/) modules in your Maven build.

# Build

    mvn clean install

# Usage

Add the following plugin inside build -> plugins:

```xml
<plugin>
    <groupId>org.mule.tools.javascript</groupId>
    <artifactId>npm-maven-plugin</artifactId>
    <version>1.0-SNAPSHOT</version>
    <executions>
        <execution>
            <phase>generate-sources</phase>
            <goals>
                <goal>fetch-modules</goal>
            </goals>
            <configuration>
                <packages>
                    <package>colors:0.5.1</package>
                    <package>jshint:0.8.1</package>
                </packages>
            </configuration>
        </execution>
    </executions>
</plugin>
```

By default modules are downloaded recursively in `src/main/resources/META-INF` but other path can be specified with the 'outputDirectory' parameter. 

# Authors
Alberto Pose (@thepose)

# License
Copyright 2012 MuleSoft, Inc.

Licensed under the Common Public Attribution License (CPAL), Version 1.0.
    
### Happy hacking!
