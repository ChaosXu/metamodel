## Thank you!

Before anything else, thank you. Thank you for taking some of your precious time helping this project move forward.

This guide will help you get started with Apache MetaModel's development environment. You'll also find the set of rules you're expected to follow in order to submit improvements and fixes to Apache MetaModel.

## Starter issues to work on

If you're looking for a relevant issue to work on, we suggest you to do the following:

* Join the @dev mailing list (send a mail to dev-subscribe@metamodel.incubator.apache.org, then afterwards communicate via dev@metamodel.incubator.apache.org).
* Check the issues in JIRA with the 'starter' label: https://issues.apache.org/jira/issues/?jql=project%20%3D%20METAMODEL%20AND%20labels%20%3D%20starter
* If you have something else on your mind, make yourself heard on the @dev mailing list.


## Build the code

Fork and clone the repository:

```
> git clone https://git-wip-us.apache.org/repos/asf/incubator-metamodel.git MetaModel
```

Try your first build:

```
> cd MetaModel
> mvn clean install
```

## About tests

By default the build will include all self-contained tests, including some quick integration tests to embedded databases like H2, Derby, HSQLDB etc.

Some tests have external dependencies to running servers etc. Those tests can be configured by adding a file called **metamodel-integrationtest-configuration.properties** to your local user's home folder. You can take a look at the [example-metamodel-integrationtest-configuration.properties file](https://raw.githubusercontent.com/apache/incubator-metamodel/master/example-metamodel-integrationtest-configuration.properties) to see which properties are available in order to configure the external server connections.

## Coding guidelines

If you plan on submitting code, read this carefully. Please note it is not yet complete.

We stick to the [Google Java Style Guide](http://google-styleguide.googlecode.com/svn/trunk/javaguide.html), with a few modifications/exceptions:

* We often prefix instance variables with an underscore (_). This to easily distinguish between method local and instance variables, as well as avoiding the overuse of the 'this' keyword in e.g. setter methods.
* We format indentation using spaces, not tabs. We use 4 spaces for each indentation.
* We format line wrapping using a desired max line length of 120 characters.