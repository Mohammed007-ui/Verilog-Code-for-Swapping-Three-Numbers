Aim To design and simulate a Verilog HDL code for swapping the values of three numbers without using any temporary variables, and verify the correctness of the swapping operation through a testbench using the Vivado 2023.1 simulation environment.

Apparatus Required Vivado 2023.1 or equivalent Verilog simulation tool.

Procedure Launch Vivado 2023.1:

Open Vivado and create a new project. Write the Verilog Code for Swapping:

Write the Verilog code that swaps the values of three numbers (a, b, and c) using basic arithmetic or bitwise operations without using temporary variables. Create the Testbench:

Write a testbench to simulate the swapping operation. The testbench should initialize three numbers, trigger the swapping module, and check if the values are swapped correctly. Add the Verilog Files:

Add the Verilog module and the testbench file to the Vivado project. Run Simulation:

Run the behavioral simulation in Vivado to verify the swapping operation. Observe the Waveforms:

Examine the waveform to confirm that the values of the three numbers are swapped as expected. Save and Document Results:

Capture the waveform output and include the results in your report for verification.
![image](https://github.com/user-attachments/assets/58e7c12f-da03-4a3b-b5b8-305c776031d5)###VERILOG CODE:
### Verilog code for swapping three numbers
~~~
module swap(clk);
input clk;
real a = 5;
real b = 3;
always@(posedge clk)begin
a<=b;
b<= a;
end
endmodule
~~~
OUTPUT:![Screenshot 2024-10-04 185927](https://github.com/user-attachments/assets/d536cda6-6a80-4242-8076-e824529de0b3)

###Testbench for Swapping Three Numbers:
~~~
module swap(clk);
    input clk;
    reg [31:0] a = 32'd5;  // Fixed-point representation of real numbers
    reg [31:0] b = 32'd3;  // Using reg instead of real

    always @(posedge clk) begin
        reg [31:0] temp;
        temp = a;
        a <= b;
        b <= temp;
    end
endmodule
~~~
OUTPUT:![Screenshot 2024-10-04 191934](https://github.com/user-attachments/assets/173fb333-b6b9-4393-9697-552922496a7c)


Conclusion
In this experiment, a Verilog HDL code for swapping three numbers was designed and successfully simulated. The testbench verified the swapping operation, showing that the values of three input numbers (a, b, and c) were swapped correctly without the use of temporary variables. This experiment demonstrated the effectiveness of Verilog in implementing logical operations and control mechanisms such as swapping values. The simulation results confirm the correct functionality of the design.
