
# Contents

1. [FPGA Tools](#about_tool)
2. [Compiling and Installing the Tool](#tool_setup)
3. [Using the Tool](#tool_usage)
4. [Example: Loading an FPGA Image](#load_fpga)
5. [Uninstalling the Tool](#tool_unistall)

<a name="about_tool"></a>
# FPGA Tools
FpgaCmdEntry is a part of the FPGA development suite and implements FPGA image loading, loading status query, and device information query functions. The following shows the directory structure of FPGA tools:

	linux-htucef:/home/huaweicloud-fpga/fp1/tools/fpga_tool # ll
	total 20
	drwxr-x--- 2 root root 4096 Nov 20 20:07 build
	drwxr-x--- 2 root root 4096 Nov 20 20:07 docs
	-rw-r----- 1 root root 1579 Nov 20 20:07 LICENSE.txt
	-rw-r----- 1 root root 3530 Nov 20 20:07 README.md
	drwxr-x--- 3 root root 4096 Nov 20 20:07 src



[Folder *src*](./src/) stores the source code of the FPGA tool.

[Folder *build*](./build/) stores script files for tool compilation, installation, and uninstallation.

[Folder *docs*](./docs/) stores tool description documents.

[*LICENSE.txt*](./LICENSE.txt) License file

[*README.md*](./README.md) Loading tool documentation


**Note:**

1. Before using this tool, compile and install it by following the compilation and installation guide.
2. After the installation is complete, implement the loading and query functions by following the instructions in the operation guide.

<a name="tool_setup"></a>
# Compiling and Installing the Tool
Take the following steps:

Step 1: Before the compilation and installation, run the `gcc --version` command to check whether the GCC is installed(The FPGA tool compilation depends on the GCC).
	
	linux-htucef:/ # gcc --version
	gcc (GCC) 4.8.5 20150623 (Red Hat 4.8.5-16)
	Copyright (C) 2015 Free Software Foundation, Inc.
	This is free software; see the source for copying conditions.  There is NO
	warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.

Step 2: Before the compilation and installation, check that the root permission is obtained.

Step 3: Go to **[fp1](../../)** and run the `bash fpga_tool_setup.sh` command to compile and install the tool.
	
	linux-htucef:/home/huaweicloud-fpga/fp1 # bash fpga_tool_setup.sh 
	FPGA_TOOL SETUP MESSAGE:Done setting environment variables.
	Entering /home/huaweicloud-fpga/fp1/tools/fpga_tool/build/../src
	rm -rf /home/huaweicloud-fpga/fp1/tools/fpga_tool/src/../dist/tool_obj 
	rm -f  /home/huaweicloud-fpga/fp1/tools/fpga_tool/src/../dist/FpgaCmdEntry
	gcc -c ...
	...
	finish FpgaCmdEntry
	FPGA_TOOL SETUP MESSAGE: Build completed.
	FPGA_TOOL INSTALL MESSAGE: Executing as root...
	FPGA_TOOL INSTALL MESSAGE: Copy fpga_tool to /usr/local/bin sucess 
	FPGA_TOOL INSTALL MESSAGE: Set privilege of /usr/local/bin/FpgaCmdEntry success
	FPGA_TOOL SETUP MESSAGE: Setup fpga_tool success.

<a name="tool_usage"></a>
# Using the Tool
After the compilation and installation, you can use the FPGA tool to query the device information, load an image, and query the loading status in any directory.

[FPGA Tools Operation Instructions](./docs/load_tool_operation_instuctions.md)

<a name="load_fpga"></a>
# Example: Loading an FPGA Image
After the compilation and installation, you can use the FPGA tool to query the device information, load an image, and query the loading status in any directory.

[Loading an FPGA Image](./docs/load_an_fpga_image.md)

<a name="tool_unistall"></a>
# Uninstalling the Tool
Take the following steps:

Step 1: Before the uninstallation, check that the root permission is obtained.

Step 2: Go to [**fp1**](../../) and run the `bash fpga_tool_unistall.sh` command to uninstall the tool.

	linux-htucef:/home/huaweicloud-fpga/fp1 # bash fpga_tool_unistall.sh 
	Entering /home/huaweicloud-fpga/fp1/tools/fpga_tool/build/../src
	rm -rf /home/huaweicloud-fpga/fp1/tools/fpga_tool/src/../dist/tool_obj 
	rm -f  /home/huaweicloud-fpga/fp1/tools/fpga_tool/src/../dist/FpgaCmdEntry
	FPGA_TOOL CLEAN MESSAGE:Clean success
	FPGA_TOOL UNISTALL MESSAGE: Unistall completed.




\----End