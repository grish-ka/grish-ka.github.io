IotaOS
######
IotaOS is a Monolithic Kernel based operating system designed for embedded systems and IoT devices. It provides a lightweight and efficient platform for running applications on resource-constrained hardware.

Key Features
 - Monolithic Kernel architecture: IotaOS is built on a Monolithic Kernel architecture, which allows for better modularity and separation of concerns. This design enables developers to create custom drivers and services without affecting the core kernel.
 - Filesystem: IotaOS includes a simple filesystem that supports basic file operations such as reading, writing, and deleting files. The filesystem is designed to be lightweight and efficient, making it suitable for embedded systems with limited storage capacity.
 - Executer: The executor in IotaOS is responsible for managing the execution of tasks and processes. It provides scheduling and context switching capabilities, allowing multiple tasks to run concurrently on the system.
 - Custom executable format: IotaOS supports a custom executable format that is optimized for embedded systems. This format allows for efficient loading and execution of applications, while also providing support for features such as dynamic linking and shared libraries.

Iosh
****
Iosh is a shell interface for IotaOS that provides a command-line interface for interacting with the operating system. It allows users to execute commands, manage files, and perform various system operations. Iosh is designed to be simple and user-friendly, making it easy for developers and users to interact with IotaOS. It provides a set of built-in commands for common tasks, as well as support for custom commands that can be added by developers. Iosh is an essential component of the IotaOS ecosystem, providing a convenient way for users to interact with the operating system and manage their applications.
here is the set of built-in commands in Iosh:

+-------------+-----------------------------------------------------------+
| Command     | Description                                               |
+=============+===========================================================+
| ``help``    | Shows a list of available commands and their descriptions |
+-------------+-----------------------------------------------------------+
| ``ls``      | Lists files in the ramdisk                                |
+-------------+-----------------------------------------------------------+
| ``run``     | Executes an .ib file (e.g. './test.ib')                   |
+-------------+-----------------------------------------------------------+
| ``meminfo`` | Shows physical memory usage information                   |
+-------------+-----------------------------------------------------------+
| ``version`` | Shows the kernel and shell version                        |
+-------------+-----------------------------------------------------------+
| ``clear``   | Clears the terminal screen                                |
+-------------+-----------------------------------------------------------+
| ``reboot``  | Reboots the system                                        |
+-------------+-----------------------------------------------------------+
| ``exit``    | Exits the shell and shuts down the system                 |
+-------------+-----------------------------------------------------------+

``.ib`` files
*************
``.ib`` files are a custom file format used in IotaOS for storing applications. These files are designed to be lightweight and efficient, making them suitable for embedded systems with limited storage capacity. The ``.ib`` file format allows developers to easily make c (and assembly) applications for IotaOS, and provides support for features such as storing your c (or assembly) app as a ``.ib`` file, which can then be executed on the IotaOS platform. This format is optimized for the unique requirements of embedded systems, ensuring that applications can run efficiently while minimizing resource usage.

``.ib`` header
==============
The ``.ib`` (iota binary) header is a crucial component of the ``.ib`` file format used in IotaOS. It contains metadata about the application, such as the magic number (0x4249), code size, header size and entry point. The header also includes information about the ``ib_loader`` format version and other metadata required for proper execution. This allows the operating system to manage and execute the application effectively. The ``.ib`` header is designed to be compact and efficient, ensuring that it does not consume unnecessary resources while providing essential information for the execution of applications on the IotaOS platform.

here is an example of a ``.ib`` header structure:

.. code-block:: gas
   :linenos:
   :caption: extract from ``crt0.s`` (0.1.0-beta.17 version (format version 1))
   :name: ib_header_v1

   /* --- IOTA BINARY (``.ib``) HEADER --- */
   /* This data is at Byte 0 */
   .short 0x4249       /* magic 'IB' */
   .short 1            /* version */
   .long  16           /* offset to code */
   .long  bin_end - .  /* total size */
   .long  0            /* entry point */

.. version-added:: 0.1.0-beta.17
   The ``.ib`` file format and its header structure were introduced in this version of IotaOS. This addition allows developers to create and manage applications in a standardized format, enhancing the overall functionality and usability of the IotaOS platform.

*Table of format versions and code examples:*

+----------------+---------------------+
| format version | code example        |
+================+=====================+
| 1              | :ref:`ib_header_v1` |
+----------------+---------------------+

.. github::

    you can find the source code for this project here:

    .. button-link:: https://github.com/grish-ka/IotaOS
        :color: primary
        :outline:

        :octicon:`mark-github`

v0.1.0 coming soon (as of 01/3/2026)! Maybe tonight, maybe tomorrow, maybe next week, who knows ¯\_(ツ)_/¯?
Well i know tonight is the answer and the latest is v0.1.1 so go to the github and download it
can someone film it in qemu? that would be nice so I can put it into the docs and show it off, I don't have the time to do it myself right now, but if you do, please share it with me so I can add it to the docs! Maybe put it on a github issue! I would really appreciate it! Thanks in advance! Also if you discover a bug, please report it on the github issues page! I will try to fix it as soon as possible! Thanks again for your support and interest in IotaOS!