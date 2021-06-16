==========
loggertodb
==========


.. image:: https://img.shields.io/travis/openmeteo/loggertodb.svg
        :target: https://travis-ci.org/openmeteo/loggertodb

.. image:: https://codecov.io/github/openmeteo/loggertodb/coverage.svg
        :target: https://codecov.io/gh/openmeteo/loggertodb
        :alt: Coverage

.. image:: https://img.shields.io/pypi/v/loggertodb.svg
        :target: https://pypi.python.org/pypi/loggertodb

.. image:: https://readthedocs.org/projects/loggertodb/badge/?version=latest
        :target: https://loggertodb.readthedocs.io/en/latest/?badge=latest
        :alt: Documentation Status

.. image:: https://pyup.io/repos/github/openmeteo/loggertodb/shield.svg
     :target: https://pyup.io/repos/github/openmeteo/loggertodb/
     :alt: Updates



Insert meteorological station data to Enhydris using the `webservice api`

License
=======

Free software: GNU General Public License v3

Documentation
=============

https://loggertodb.readthedocs.io.

Creating a Windows executable
=============================

**Note:** You have to work on Windows 7. If you work on Windows 10, the
resulting executable might not run on Windows 7. If you find a way to
create the executable on Windows 10 that runs on Windows 7 (or stop
supporting Windows 7), fix this README.

We've found that executables created on 64-bit Windows 7 do run on
32-bit Windows 7, however ideally the resulting executable should be
tested in both environments.

The first time:

 1. Install ``git``.
 2. `(a)` Install a recent Python 3 version. `(b)` Install virtualenv
 3. Execute Git Bash.
 4. Clone `loggertodb_` 
 5. Change to the working directory of ``loggertodb``.
 6. ``pip install virtualenv==16.1.0`` (this is because of a
    `pyinstaller bug`_).
 7. ``virtualenv ..\venv``
 8. ``..\venv\Scripts\pip install -e .``
 9. ``..\venv\Scripts\pip install pyinstaller``
 10. ``..\venv\Scripts\python setup.py test``
 11. ``..\venv\Scripts\pyinstaller --onefile --name=loggertodb bin/loggertodb-windows``

.. _pyinstaller bug: https://github.com/pyinstaller/pyinstaller/issues/4064
.. _loggertodb: https://github.com/openmeteo/loggertodb

Next times:

 1. ``../venv/Scripts/pip install -e .`` (to upgrade dependencies if needed)
 2. ``../venv/Scripts/python setup.py test``
 3. ``rm -r dist loggertodb.spec``
 4. ``../venv/Scripts/pyinstaller --onefile --name=loggertodb bin/loggertodb-windows``

After this, ``loggertodb.exe`` should be in the ``dist`` directory.


Creating a Windows executable via vagrant
------------------------------------------

This is a Windows 7 (32bit) Box that is derived from a box provided by
microsoft on [Modern.IE](https://developer.microsoft.com/en-us/microsoft-edge/tools/vms/windows) with a 10 day evaluation licence or use this
["IE11 on Win7" Vagrant Box with build number 20150916](https://az792536.vo.msecnd.net/vms/VMBuild_20150916/Vagrant/IE11/IE11.Win7.Vagrant.zip) adapted to match vagrant's requirements:

 * User is 'vagrant' (password 'vagrant')
 * WinRM is activated (for ``vagrant powershell``)
 * RDP is activated (for ``vagrant rdp``)
 * SSH is activated (for ``vagrant ssh``)
 * chocolately is installed for easy unattended software installations
 * Windows Defender is disabled to avoid unnecessary load


Easy install  on an vagrant
--------------------------------
* Download from [here](https://az792536.vo.msecnd.net/vms/VMBuild_20150916/Vagrant/IE11/IE11.Win7.Vagrant.zip)
* Unpack "IE11 - Win7.box" in ZIP-file to project directory
* run ``vagrant box add "IE11 - Win7.box" --name IE11Win7`` or
* rename box to "IE11-Win7.box" and run ``vagrant box add  file:///C:/path/to/file.box/IE11-Win7.box  --name IE11Win7 ``
* run ``vagrant up`` (wait for timeout message!)


The first time:

 1. Install ``git``.
 2. `(a)` Install a recent Python 3 version. `(b)` Install virtualenv
 3. Execute Git Bash.
 4. Clone loggertodb. (https

Unpack "IE11 - Win7.box" in ZIP-file to project directory
run vagrant box add "IE11 - Win7.box" --name IE11Win7
run vagrant up (wait for timeout message!)

It is adapted to match vagrant's requirements:

User is 'vagrant' (password 'vagrant')
WinRM is activated (for vagrant powershell)
RDP is activated (for vagrant rdp)
SSH is activated (for vagrant ssh)
chocolately is installed for easy unattended software installations
Windows Defender is disabled to avoid unnecessary load





