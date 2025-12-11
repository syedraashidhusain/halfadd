[rtl.pdf](https://github.com/user-attachments/files/24106478/rtl.pdf)HALF_ADDER_SUBTRACTOR Implementation-of-Half-Adder-and-Half Subtractor-circuit

AIM:

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

Equipments Required:

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

Half Adder

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB image

<img width="565" height="283" alt="image" src="https://github.com/user-attachments/assets/d6b26f98-3459-4bce-a5f6-eb0920d5e4f0" />


Figure -01 HALF ADDER

Half Subtractor

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.

![WhatsApp Image 2025-12-11 at 9 16 11 PM](https://github.com/user-attachments/assets/b299030c-8c65-4733-abe1-1386deb9720b)


Diff = A’B+AB’ =A ⊕ B Borrow = A’B image

Figure -02 HALF Subtractor

Truthtable

HALF ADDER 

<img width="753" height="418" alt="image" src="https://github.com/user-attachments/assets/1ab9ec15-0af9-46e8-81be-44be7b9092d5" />


HALF SUBTRACTOR 

<img width="761" height="418" alt="image" src="https://github.com/user-attachments/assets/00c215d6-e4f3-488b-b3f6-9be6e20cc245" />


Procedure

Type the program in Quartus software.

Compile and run the program.

Generate the RTL schematic and save the logic diagram.

Create nodes for inputs and outputs to generate the timing diagram.

For different input combinations generate the timing diagram.

Program:
```

module half_adder (
    input  wire a, b,     // Inputs
    output wire sum,      // Sum output
    output wire carry     // Carry output
);

    // Logic equations
    assign sum   = a ^ b;   // XOR for sum
    assign carry = a & b;   // AND for carry

endmodule


module half_subtractor (
    input  wire a, b,         // Inputs
    output wire diff, borrow  // Outputs
);

    // Logic equations
    assign diff   = a ^ b;     // XOR for difference
    assign borrow = ~a & b;    // Borrow when a < b
```
Developed by: SYED RAASHID HUSAIN  M

RegisterNumber: 25009038
[rtl.pdf](https://github.com/user-attachments/files/24106485/rtl.pdf)

[rtl img.pdf](https://github.com/user-attachments/files/24106536/rtl.img.pdf)




Output/TIMING Waveform wave 

[wave img.bmp](https://github.com/user-attachments/files/24106525/wave.img.bmp)
[wave img.bmp](https://github.com/user-attachments/files/24106540/wave.img.bmp)

Result:

The code is excecuted successfully.
