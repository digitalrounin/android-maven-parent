
Generating Maven Site Report
============================

    mvn clean verify site -Danalyze.skip=false -Danalyze.failfast=false


Dependency Version Report
=========================

http://mojo.codehaus.org/versions-maven-plugin/

To display what needs to be updated from CLI:

    mvn versions:display-plugin-updates versions:display-dependency-updates versions:display-property-updates


To update **dependencies** to the latest verions:

    mvn versions:use-latest-releases

Note that it only updates dependencies, not plugin versions.  Seems like plugin
versions have to be maintained manually.

Read the following for more information:

- http://mojo.codehaus.org/versions-maven-plugin/examples/advancing-dependency-versions.html

Do not for get to run *mvn site* and check the site pages for the projects for
more verion information.

Dependency Tree
===============

    mvn dependency:tree

