A reproducer project

###

```
./gradlew help
```

fails with:

```
./gradlew help         
Isolated projects is an incubating feature.
Calculating task graph as configuration cache cannot be reused because file 'lib/build.gradle.kts' has changed.

> Task :help

Welcome to Gradle 9.1.0.

To run a build, run gradlew <task> ...

To see a list of available tasks, run gradlew tasks

To see more detail about a task, run gradlew help --task <task>

To see a list of command-line options, run gradlew --help

For more detail on using Gradle, see https://docs.gradle.org/9.1.0/userguide/command_line_interface.html

For troubleshooting, visit https://help.gradle.org

[Incubating] Problems report is available at: file:///Users/rafael/sources/repros/shadow-reproducer/build/reports/problems/problems-report.html

FAILURE: Build failed with an exception.

* What went wrong:
Configuration cache problems found in this build.

1 problem was found storing the configuration cache.
- Plugin 'com.gradleup.shadow': Project ':lib' cannot dynamically look up a property in the parent project ':'

See the complete report at file:///Users/rafael/sources/repros/shadow-reproducer/build/reports/configuration-cache/44xd8gdnk61s0q27t55gyyk79/jlkx29ygkee89vr047ecsylw/configuration-cache-report.html
> Project ':lib' cannot dynamically look up a property in the parent project ':'

* Try:
> Run with --stacktrace option to get the stack trace.
> Run with --info or --debug option to get more log output.
> Run with --scan to generate a Build Scan (Powered by Develocity).
> Get more help at https://help.gradle.org.

BUILD FAILED in 513ms
1 actionable task: 1 executed
Configuration cache entry discarded with 1 problem.
```
