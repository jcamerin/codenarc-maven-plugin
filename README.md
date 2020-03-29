codenarc-maven-plugin
=====================

Forked from https://github.com/gleclaire/codenarc-maven-plugin

Maven Mojo Plug-In to generate reports based on the CodeNarc Analyzer

Run all test
mvn -Prun-its clean install

Skip tests
mvn -DskipTests=true clean install

Run selected tests example
mvn -Prun-its -Dinvoker.test=basic-1 clean install

Run tests on CodeNarc test source code that is local instead of from SVN repository
mvn -o -DtestSrc=local -DlocalTestSrc=/opt/CodeNarc/CodeNarc-0.17/src/test -Prun-its clean install

Run tests in debugger
mvn -Dmaven.surefire.debug="-Xdebug -Xrunjdwp:transport=dt_socket,server=y,suspend=y,address=8000 -Xnoagent -Djava.compiler=NONE" -o -DtestSrc=local -DlocalTestSrc=/opt/CodeNarc/CodeNarc-0.17/src/test -Prun-its clean install
 
