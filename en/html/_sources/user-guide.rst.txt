User Guide
==========

.. toctree::
   :maxdepth: 1

Prerequisites
-------------

* Java 1.7 or 1.8(Java 9 and above haven't been verified yet)
* Maven
* `protoc 2.5.0 <https://github.com/protocolbuffers/protobuf/releases/tag/v2.5.0>`_

Build
-----

Build distribution tarball
~~~~~~~~~~~~~~~~~~~~~~~~~~

Go to the project root, and run

.. code-block:: bash

    mvn clean package -Dmaven.test.skip

Each module of the project can also be built separately.

Build source code
~~~~~~~~~~~~~~~~~

If you want to build and debug source code in IDE, go to the project root, and run

.. code-block:: bash

    mvn compile

This command will generate the Java source files from the ``protoc`` files, the generated files located in ``target/generated-sources``.

When this command finished, you can use IDE import the project as maven project.

Deploy
~~~~~~

After the build, please go to ``tubemq-server/target``. You can find the **tubemq-server-x.x.x-bin.tar.gz** file. It is the server deployment package, which includes scripts, configuration files, dependency jars and web GUI code.

For the first time deployment, we just need to extract the package file. For example, we put these files into the ``/opt/tubemq-server``, here's the folder structure.

::

    /opt/tubemq-server
    ├── bin
    ├── conf
    ├── lib
    ├── logs
    └── resources
