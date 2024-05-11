The purpose of this project is to hightlight an issue with using test-jar classes as dependencies in compile scope, with VsCode. Specifically the java test-runner.

By default test-jar dependencies are not included in the classpath in VsCode. By disabling this default, via the following property: `"java.import.maven.disableTestClasspathFlag": true`, the following occurs:

* The syntax error highlighting withn VsCode are no longer present and the editor will detect the class files.
* The test-runner's gutter icon is removed and tests can no longer be run from within the editor
* The Test Explorer no longer detects any test classes and no test can be run from the Test Explorer

It should also be noted that, running the test via command line with `./mvnw install` produces no compiler errors and the tests are run without issue; with or without the above setting changed.
