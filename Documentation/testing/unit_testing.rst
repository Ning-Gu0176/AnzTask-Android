=========
Unit Test
=========

Android Studio Unit Test
========================

Android Studio provides with very convenient way for unit test. If you don’t know how to set up unit test in Android Studio, ``How-to guides`` section will help you to get start.

AnzVolley Test Case
===================

The main functionality of AnzVolley is making RESTful request and parsing response JSON object, so unit test should include testing all different RESTful requests.Since AnzVoley makes asynchronous request, a limited time out loop should be used for testing. Further more, any unit functionality should have separated test case as well.

.. warning:: internet permission must be added into AnzVolley module’s AndroidManifest file since the test involves networking. Otherwise the test case will definitely fail.

AnzVolley module test cases include:

 - testEarthquakeData (test the RESTful request of earthquake data)
 - testBuildingNamePairsWithoutProperty (test the name pairs building logic)
 - testBuildingNamePairsWithProperty (test the name pairs building logic)

.. note:: 

 - Test case name might be different from above. refer to project/AnzVolley/src/androidTest for the test source code.
 - To test private method of AnzVolley, reflection can be used. If test team has access to the source code, just change private method to public method.  

ANZ Task Test Case
==================

ANZ Task app source code includes all Android pure stuff like UI, navigation and some java logic. To test ANZ Task app module, the best choice would be functional testing even though we still can test some logic unit like utility code.

Anz Task app module test cases include:

 - testComparatorMagnitudeAscending (test comparator of magnitude property in ascending order)
 - testComparatorMagnitudeDescending (test comparator of magnitude property in descending order)

 - testComparatorDepthAscending (test comparator of depth property in ascending order)
 - testComparatorDepthDescending (test comparator of depth property in descending order)

.. note:: 

 - Test case name might be different from above. refer to project/app/src/androidTest/unit for the test source code.

Test Report
===========

 - `AnzVolley Test Report <../_static/test_report/TR-AnzVolleyUnitTest.html>`_
 - `Anz Task Test Report <../_static/test_report/TR-AnzTaskUnitTest.html>`_
