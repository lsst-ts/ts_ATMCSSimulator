.. py:currentmodule:: lsst.ts.ATMCSSimulator

.. _lsst.ts.ATMCSSimulator.version_history:

###############
Version History
###############

v1.1.1
======

* Updated Jenkinsfile.conda to Jenkins Shared Library
* Pinned the version of ts-idl and ts-salobj in conda recipe

v1.1.0
======

Changes:

* Updated for ts_salobj 6.1.
* Updated `ATMCSCsc.set_event` to return ``did_put``, for debugging.
* Defined `ATMCSCsc` class variable ``valid_simulation_modes`` to eliminate a deprecation warning.
* Remove deprecation warnings caused by calling `salobj.RemoteTopic.get` with ``flush`` specified.
* Removed obsolete travis file.

Requires:

* ts_salobj 6
* ts_simactuators 2
* ts_idl 2
* ts_xml 5 - 6
* IDL file for ATMCS, e.g. built with make_idl_files.py

v1.0.4
======

Changes:

* Update deprecated code for compatibility with ts_salobj 6 (and 5).
* Add black to conda test dependencies

Requires:

* ts_salobj 5.11 or 6.0
* ts_simactuators 1 or 2
* ts_idl 1 (for ts_salobj 5) or 2 (for ts_salobj 6)
* ts_xml 5 - 6
* IDL file for ATMCS, e.g. built with make_idl_files.py

v1.0.3
======

Changes:

* Update for compatibility with ts_salobj 5.13.

Requires:

* ts_salobj 5.11
* ts_simactuators 1.0
* ts_idl 1
* ts_xml 5
* IDL file for ATMCS, e.g. built with make_idl_files.py

v1.0.2
======

Changes:

* Add a test that code is formatted with black.
  This requires ts_salobj 5.11.
* Add a test for ``bin/run_atmcs_simulator.py``.
* Fix f strings with no {}.
* Remove ``sudo: false`` from ``.travis.yml``.

Requires:

* ts_salobj 5.11
* ts_simactuators 1.0
* ts_idl 1
* ts_xml 5
* IDL file for ATMCS, e.g. built with make_idl_files.py

v1.0.1
======

Changes:

* Include conda package build configuration.
* Added a Jenkinsfile to support continuous integration and to build conda packages.
* Fix Jenkinsfile for CI job.

Requires:

* ts_salobj 5.4
* ts_simactuators 1.0
* ts_idl 1
* ts_xml 5
* IDL file for ATMCS, e.g. built with make_idl_files.py

v1.0.0
=======

First release. No changes from v0.11.0.

Requires:

* ts_salobj 5.4
* ts_simactuators 1.0
* ts_idl 1
* ts_xml 5
* IDL file for ATMCS, e.g. built with make_idl_files.py

v0.11.0
=======

Major changes:

* Update for a change to the XML.
* Updated test_csc.py to use `lsst.ts.salobj.BaseCscTestCase`.
* Added a revision history.
* Code formatted by ``black``, with a pre-commit hook to enforce this. See the README file for configuration instructions.

Requires:

* ts_salobj 5.4
* ts_simactuators 0.1
* ts_idl 1
* ts_xml 5
* IDL file for ATMCS, e.g. built with make_idl_files.py

v0.10.1
=======

Major changes:

* Added jenkins build.

Requires:

* ts_salobj 5.2
* ts_simactuators 0.1
* ts_idl 1
* IDL file for ATMCS, e.g. built with make_idl_files.py

v0.10.0
=======

Major changes:

* Update to use ts_simactuators.
* Update unit tests to use asynctest.

Requires:

* ts_salobj 5.2
* ts_simactuators 0.1
* ts_idl 1
* IDL file for ATMCS, e.g. built with make_idl_files.py

v0.9.0
======

Major changes:

* Update for ts_salobj 5.2.
* Use simulation_mode instead of initial_simulation_mode

Requires:

* ts_salobj 5.2
* ts_idl 1
* IDL file for ATMCS, e.g. built with make_idl_files.py

v0.8.3
======

Make bin/run_atmcs_simulator.py executable (chmod +x).

Requirements:
* ts_salobj 4.5 or 5
* ts_idl
* IDL file for ATMCS, e.g. built with make_idl_files.py

v0.8.2
======

Major changes:

* Allow using the package without scons.

Other changes:

* Fix a bug in TPVAJ.pva.
* Modernize calling `BaseCsc.fault` to simplify the code and eliminate a deprecation warning.

Requirements:

* ts_salobj 4.5 or 5
* ts_idl
* IDL file for ATMCS, e.g. built with make_idl_files.py

v0.8.1
======

* Make sure M3 moves always display "in motion" state.
* Fix a unit test broken by a new generic event.

Requirements:

* ts_salobj v4.4
* ts_idl
* IDL file for ATMCS, e.g. built with make_idl_files.py

v0.8.0
======

Major changes:

Output the new positionLimits event.

Requirements:

* ts_salobj v4.4
* ts_idl
* IDL file for ATMCS, e.g. built with make_idl_files.py

v0.7.0
======

Major changes:

* Update for changes to ATMCS topics
* Most telemetry topic fields are now arrays.
* Added a few fields to the trackTarget command and target event.

Requirements:

* ts_salobj v4.4 or later
* ts_idl
* ATMCS IDL files, e.g. built with make_idl_files.py

v0.6.0
======

Major changes:

* Use OpenSplice dds.
* Do not enable unused axes.

Requirements:

* ts_salobj 4
* ts_idl
