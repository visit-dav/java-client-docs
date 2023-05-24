# java-client-docs

We do not expect to have to update the Java Client docs very often.
As a result, none of this is automated.
But, its pretty simple too.

The goal is to update all the `*.html` and `*.css` files here in the `docs` directory of the `main` branch with the most up to date material.
This can be done in a few ways.

1. Obtain the most recent Java release, such as [jvisit3.3.3.tar.gz](https://github.com/visit-dav/visit/releases/download/v3.3.3/jvisit3.3.3.tar.gz), and simply recursively copy the entire contents of the `docs` subdirectory from the release to the same directory in this repo.
1. Run `make visit_java_docs` in the `src/java` directory and recursively copy the entire contents of the resulting `docs` directory to the same directory in this repo.
1. Run `javadoc -notimestamp -d docs <path-to-visit-src-java-dir>/*.java` and then also `copy <path-to-visit-src-java-dir>/stylesheet.css docs/.`
