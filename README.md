# Basys3-FPGA
Xilinx Atrix-7 Basys3 FPGA, by Digilent

Steps to PERFORM:

Launch Vivado.
On the welcome screen, click Create Project.
Click Next. Name your project (YOUR_PROJECT_NAME) and choose a location(MAKE_SURE_ENTIRE_LOCATION_HAS_NO_SPACE_IN_IT). Click Next.
For Project Type, select RTL Project and ensure "Do not specify sources at this time" is checked. Click Next.
This is the most crucial step in the setup process. Click the Boards tab. If you installed the board files correctly, you should be able to search for and select Basys3. Click Next.
Review the summary and click Finish.
Vivado will now create a project configured specifically for your board.
In the Sources panel on the left, right-click on Design Sources and select Add or Create Design Sources.
Click Create File. Set file type and name. Click OK, then Finish.
Vivado will ask you to define the module ports. You can click OK, and we'll define them directly in the file.
Write the code.
The Verilog code defines what the circuit does, but it doesn't know where the signals (defined in code) connect to the physical pins of the FPGA chip. The constraints file maps them.
In the Sources panel, right-click on Constraints and select Add or Create Constraints.
Click Create File. Name the file basys3_pins and click OK, then Finish.
The basys3_pins.xdc file will be created. Double-click it to open.
Synthesize, Implement, and Generate Bitstream
This three-step process converts our human-readable code into a final file (.bit file) that the FPGA can understand and use to configure itself.
In the Flow Navigator on the very left of the screen, scroll down to the Program and Debug section.
Click on Generate Bitstream.
Vivado will prompt you that Synthesis and Implementation need to be run first. Click Yes.
Vivado will now work through all the necessary steps. This may take a few minutes. You can monitor the progress in the top-right corner of the window.
When it's finished successfully, a dialogue box will appear. You can just click Cancel on this for now.
Now we'll load the generated bitstream file onto your FPGA.
Connect your Basys 3 board to your computer with the Micro-USB cable and make sure the power switch is turned ON.
In the Flow Navigator, at the bottom, click Open Hardware Manager.
A green bar will appear at the top of the screen. Click Open Target and then select Auto Connect.
Vivado should detect your Basys 3 board. It will appear in the Hardware Manager window.
Right-click on your FPGA device (it will have a name like xc7a35t...) and select Program Device.
A dialogue box will appear. The bitstream file should already be selected.
Click Program.
After a moment, the programming will complete. Look at your Basys 3 board.
Congratulations, you've successfully programmed your FPGA design!!!
