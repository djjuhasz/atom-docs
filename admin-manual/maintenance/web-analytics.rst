.. _maintenance-web-analytics:

=============
Web analytics
=============

According to `Wikipedia <https://en.wikipedia.org/wiki/Web_analytics>`__, web
analytics is "*the measurement, collection, analysis and reporting of internet
data for purposes of understanding and optimizing web usage.*"

There are two main technological approaches to collecting the data: logfile
analysis, which reads the logfiles in which the web server records all its
transactions; and page tagging, which uses JavaScript on each page to notify a
third-party server when a page is rendered by a web browser.

.. TIP::
  If your analytics tracker is not working, try turning debugging on and off again
  via index.php. The analytics code should appear in 'View Source'.


Logfile analysis tools
======================

These types of tools require access to the log files generated by the web server.

* AWStats: http://awstats.sourceforge.net/
* Webalizer: http://www.webalizer.org/


Page tagging tools
==================

The tools found under this section require only that a system administrator or developer
insert a JavaScript code snippet into the relevant page int AtoM where you'd
like to gather analytic data. Probably the best known open source solution is
`Piwiki <http://piwik.org/>`_.

You should be able to configure any solution in AtoM by editing the
corresponding `PHP templates <https://github.com/artefactual/atom/tree/2.x/apps/qubit/templates>`_.

As of AtoM 2.0.0, you can configure Google Analytics just adding your tracking
ID to the app.yml configuration file. Open your favorite text editor and add the
following contents in it:

.. code-block:: yaml

   all:
     google_analytics_api_key: UA-XXXXX-X

Replace UA-XXXXX-X with your tracking ID. Once you are done, remember to
:ref:`clear the cache <maintenance-clear-cache>`.
