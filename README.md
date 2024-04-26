Overview
This project aims to build an FPGA-based egg timer by combining various digital design elements such as counters, 
finite state machines, encoders, registers, and logic. The egg timer will utilize inputs including a 100MHz clock, push buttons 
(BTNL/BTNR/BTNU/BTND), and slide switches (SW0/SW15), while outputs will include LEDs (LED0/LED1) and control signals for four seven-segment 
displays. The timer will display cook time in minutes and seconds, allowing users to set and adjust the time, start the timer, 
and monitor its progress.

Features
Functionality:
Display cook time in minutes and seconds on seven-segment displays.
LED0 indicates timer enable status.
LED1 blinks at a 1-second interval when the timer is active.

User Interaction:
Pressing and holding BTNL allows for changing the programmed cook time using BTNU and BTND.
BTNR starts the countdown.
SW0 enables or disables the egg timer.
SW15 resets the timer circuits and sets the programmed cook time to 00:00.
Clocking:
Utilizes a 100MHz clock divided down to 5MHz and further to generate a 1Hz control signal.
Reset:
Provides a reset signal to relevant blocks.
Debounce:
Filters BTNU/BTND signals to generate debounced versions.
Master Controller:
Manages timer enable status and control signals for other blocks.
Timer On:
Controls LED1 blinking at a 0.5Hz rate during active countdown.
Count Time:
Divides the 1Hz control signal to generate a 1/60Hz signal for minutes counter.
Allows programmable count time with proper handling of button inputs.
7 Segment/LED15 Mux:
Selects data to display on seven-segment displays based on control signals.
7 Segment Display Driver:
Generates control signals to drive the four-digit seven-segment display.
Design Considerations
Block Design:
Plan and refine block design before coding.
Clock Management:
Use 5MHz clock for flip-flops; utilize 1Hz control signal for specific operations.
Debouncing:
Implement debounce circuits for reliable button input.
Error Handling:
Ensure programmed values stay within valid range.
Debugging:
Display faster time for initial debugging before switching to slower operation.
Hardware vs. Software:
Emphasize hardware-based solution for learning, acknowledging the advantages of microcontroller-based systems in certain scenarios.
Innovation

Additional Features:
Enhance timer functionality or utilize additional FPGA board features.
Explore integration with memory blocks, VGA output, audio output, additional displays, LEDs, buttons, switches, UART/USB/Ethernet interfaces, or PMOD connectors with external modules.
Utilize Vivado's built-in IP blocks, including microblaze controller for advanced features.

Conclusion
This project provides a hands-on learning experience in digital design and FPGA programming, culminating in a functional egg timer circuit with potential 
for further enhancements and integrations. By understanding the design process and exploring additional features, 
participants gain valuable skills applicable to various embedded systems applications.


































































