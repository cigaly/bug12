To reproduce bug use:

./gradlew clean build

or
gradlew.bat clean build  (on windows)

Result is similar to:

cigaly@agram:~/workspace/bug12$ ./gradlew clean build

> Task :javadoc FAILED
/home/cigaly/workspace/bug12/src/main/java/test/package-info.java:1: error: unknown tag: NamedQuery
@NamedQuery(name = "q1", query = "select something from somwhere where anything>1")
^
/home/cigaly/workspace/bug12/src/main/java/test/package-info.java:1: error: bad use of '>'
@NamedQuery(name = "q1", query = "select something from somwhere where anything>1")
                                                                               ^
2 errors

FAILURE: Build failed with an exception.

* What went wrong:
Execution failed for task ':javadoc'.
> Javadoc generation failed. Generated Javadoc options file (useful for troubleshooting): '/home/cigaly/workspace/bug12/build/tmp/javadoc/javadoc.options'

* Try:
Run with --stacktrace option to get the stack trace. Run with --info or --debug option to get more log output. Run with --scan to get full insights.

* Get more help at https://help.gradle.org

BUILD FAILED in 2s
4 actionable tasks: 4 executed
