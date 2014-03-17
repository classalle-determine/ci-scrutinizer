Scrutinizer CI Documentation
============================

Getting Started
---------------
scrutinizer ci is a hosted continuous inspection service for open-source as well as private code.

It runs static code analysis tools, runtime inspectors, and can also run your very own checks in your favorite language.

Inspections can be triggered manually, through Git pushes, or also for GitHub pull requests. Depending on how an
inspection is triggered, scrutinizer does not scan your entire project, but only those parts that changed which provides
you with highly relevant information. Furthermore, scrutinizer ci employs algorithms to filter out noise that you have
previously ignored.

Scrutinizer also collects code metrics like the cyclomatic complexity, or the length of your classes. It uses these
metrics to calculate a ranking for the different elements of your code. This helps for example in finding the areas
with the highest technical debt in your code. Learn more about :doc:`code rating <code_rating_system>`.

Supported Languages and Analyses
--------------------------------
Below, is the list of languages that we support at the moment. In addition, you can also always run custom commands as
long as their output format is among our supported formats.

Finally, we always love to add built-in support for more languages. If we are missing your favorite language/tool, please
just `open an issue <https://github.com/scrutinizer-ci/scrutinizer/issues/new>`_.

.. toctree ::
    :hidden:

    configuration
    code_rating_system
    api/index
    refactoring/index

.. toctree ::
    :hidden:
    :glob:

    tools/javascript/index
    tools/php/index
    tools/puppet/index
    tools/ruby/index

General Analyses
~~~~~~~~~~~~~~~~

.. toctree ::
    :titlesonly:

    code_rating_system
    tools/change-tracking/index
    tools/external-code-coverage/index
    tools/automated-fixes/index
    tools/custom-commands/index

Javascript
~~~~~~~~~~
- :doc:`tools/javascript/jshint/index`


PHP
~~~
- :doc:`tools/php/code-sniffer/index`
- :doc:`tools/php/copy-paste-detector/index`
- :doc:`tools/php/cs-fixer/index`
- :doc:`tools/php/mess-detector/index`
- :doc:`tools/php/pdepend/index`
- :doc:`tools/php/php-analyzer/index`
- :doc:`tools/php/security-advisory-checker/index`


Puppet
~~~~~~
- :doc:`tools/puppet/puppet-lint/index`

Ruby
~~~~
- :doc:`tools/ruby/rubocop/index`
- :doc:`tools/ruby/rails-best-practices/index`
- :doc:`tools/ruby/flay/index`

Configuration
-------------
Scrutinizer uses configuration in Yaml format; it scans different locations for this data. Most of the time, you will define
a global base configuration where you only overwrite a few selected settings for each repository.

Learn more in the :doc:`dedicated configuration chapter <configuration>`.

API
---
Scrutinizer provides an API which you can for example use to retrieve information about your projects in a programmatic
fashion: Learn more in the :doc:`API Documentation <api/index>`.
