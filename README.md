To use it, add a plugin to your pom like

``` xml
<plugin>
  <groupId>org.skife.maven</groupId>
  <artifactId>really-executable-jar-maven-plugin</artifactId>
  <version>1.0.3</version>
  <configuration>
    <!-- value of flags will be interpolated into the java invocation -->
    <!-- as "java $flags -jar ..." -->
    <flags>-Xmx1G</flags>
    
    <!-- (optional) name for binary executable, if not set will just -->
    <!-- make the regular jar artifact executable -->
    <programFile>nifty-executable</programFile>
  </configuration>
 
  <executions>
    <execution>
      <phase>package</phase>
      <goals>
        <goal>really-executable-jar</goal>
      </goals>
    </execution>
  </executions>
</plugin>
```
