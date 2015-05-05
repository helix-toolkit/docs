=====
Build
=====

.. note:: This section is under construction. Please contribute!


Requirements
------------

- .NET 3.5 or later
- Build tool with support for Portable Class Libraries (Visual Studio 201x, MsBuild)
- StyleCop

The solutions can be opened in

- VS 2010 (with the `Portable Library Tools <http://visualstudiogallery.msdn.microsoft.com/b0e0b5e9-e138-410b-ad10-00cb3caf4981>`_ extension)
- VS 2012 (with the latest update)
- VS 2013
- VS 2013 CE
- VS 2015

VS Express does not support Portable Class Libraries, and cannot be used
to build this project. 

Depending on what platform you want to build, you may need to install extra SDKs or target framework profiles

- `.NET 3.5 <http://www.microsoft.com/en-us/download/details.aspx?id=22>`_
- `.NET 4.0 <http://www.microsoft.com/nb-no/download/details.aspx?id=17851>`_
- `.NET 4.5 <http://www.microsoft.com/nb-no/download/details.aspx?id=30653>`_
- `Portable library tools 2.0 <http://visualstudiogallery.msdn.microsoft.com/b0e0b5e9-e138-410b-ad10-00cb3caf4981/>`_
- `Microsoft .NET Portable Library Reference Assemblies 4.6 <http://www.microsoft.com/en-us/download/details.aspx?id=40727>`_
- `StyleCop <http://stylecop.codeplex.com/>`_
- `SharpDX <http://sharpdx.org/>`_
- `DirectX SDK <https://www.microsoft.com/en-us/download/details.aspx?id=6812>`_


Obtain the source code
----------------------

This project is using `Git <http://git-scm.com/>`_ distributed version
control system (DVCS). To obtain the code, it is recommended to install
one of the following Git clients

- `GitHub for Windows <https://windows.github.com/>`_
- `SourceTree <http://www.sourcetreeapp.com/|SourceTree>`_ (for Windows and Mac)
- `TortoiseGit <https://code.google.com/p/tortoisegit/>`_ (Windows shell extension)
- `Git <http://git-scm.com/>`_ (command line)

Clone the repository from ``https://github.com/helix-toolkit/helix-toolkit.git``. This can be done by the following command line:

.. sourcecode:: bat

    git clone https://github.com/helix-toolkit/helix-toolkit.git

If you don't want to use Git, you can also obtain the complete source
code as a .zip archive from the `repository page <https://github.com/helix-toolkit/helix-toolkit>`_.
Click the "Download Zip" button.


Build
-----

It should be possible to open the solution and build with Visual Studio or msbuild without any
additional steps.


Build output
------------

The build output of the *Release* configurations are placed in the
``Output/`` folder. The output of the *Debug* configurations are placed
under the ``Source/*/bin/Debug`` folders.
