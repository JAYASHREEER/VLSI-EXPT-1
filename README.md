# VLSI-EXPT-1
# SIMULATE AND SYNTHESIS LOGIC GATES,ADDERS AND SUBTRACTOR USING VIVADO

## AIM :
        To simulate and synthesis Logic Gates, Adders and Subtractor using VIVADO
## APPARATUS REQUIRED : VIVADO 2023.2
## PROCEDURE :
STEP:1 Start the Vivado, Select and Name the New project.  <br>
STEP:2 Select the device family, device, package and speed.<br>
STEP:3 Select new source in the New Project and select Verilog Module as the Source type.<br>
STEP:4 Type the File Name and Click Next and then finish button. Type the code and save it.<br>
STEP:5 Select the Behavioural Simulation in the Source Window and click the check syntax.<br>
STEP:6 Click the simulation to simulate the program and give the inputs and verify the outputs as per the truth table.<br>

## LOGIC GATES :
![image](https://github.com/JAYASHREEER/VLSI-EXPT-1/assets/166278992/2c6d36eb-a80c-4c74-ad08-eacc863d3373)
## PROGRAM :
module fs(a,b,c0,c1,c2,c3,c4,c5,c6);<br> input a,b;<br> output co,c1,c2,c3,c4,c5,c6;<br> or g1 (co,a,b);<br> and g2 (c1,a,b);<br> xor g3 (c2,a,b);<br> nand g4 (c3,a,b);<br> nor g5 (c4,a,b);<br> not g6(c5,a);<br> xnor g7 (c6,a,b);<br> endmodule
## OUTPUT : 
![image](https://github.com/JAYASHREEER/VLSI-EXPT-1/assets/166278992/07b7d512-ce4f-4fcd-b6f4-cc58e04165ee)

## HALF ADDER :
![image](https://github.com/JAYASHREEER/VLSI-EXPT-1/assets/166278992/1a765829-b8ed-4fd8-b6ae-4269e3885a72)
## PROGRAM :
module ha (a,b,s,c);<br> input a,b;<br> output s,c;<br> xor g1(s,a,b);<br> O and g2 (c,a,b);<br> endmodule
## OUTPUT :
![image](https://github.com/JAYASHREEER/VLSI-EXPT-1/assets/166278992/303b5434-023e-493c-b128-dc42aa833ad4)

## HALF SUBTRACTOR :
![image](https://github.com/JAYASHREEER/VLSI-EXPT-1/assets/166278992/ee61f522-abcf-4fb3-9cef-1925f3737e0c)
## PROGRAM :
module hs (a, b, diff, borr);<br> input a,b;<br> output diff, borr;<br> xor gl (diff,a,borr);<br> and g2 (borr, -a,b);<br> endmodule
## OUTPUT :
![image](https://github.com/JAYASHREEER/VLSI-EXPT-1/assets/166278992/93634041-5e26-4829-b4c0-cfbe9bbef8fa)

## FULL ADDER :
![image](https://github.com/JAYASHREEER/VLSI-EXPT-1/assets/166278992/c998462b-ca08-4700-837c-2190f4112a1c)
## PROGRAM :
module fa (a,b,c,sum, carry);<br> input a,b,c<br>; output sum, carry;<br> wire w1,w2,w3;<br> xor gl(wl,a,b);<br> xor g2 (w2,a,b);<br> xor g3 (sum, w1,c);<br><br> and (w3,c,w1);<br>
or g5 (carry, w3,w2);<br> endmodule
## OUTPUT :
![image](https://github.com/JAYASHREEER/VLSI-EXPT-1/assets/166278992/16cba4db-33a3-46b9-b789-0002472865a9)

## HALF SUBTRACTOR :
![image](https://github.com/JAYASHREEER/VLSI-EXPT-1/assets/166278992/461f8384-77ee-4bc5-b1b0-37166f8c3d50)
## PROGRAM :
module fs(a,b,c,diff,borrow)<br>; input a,b,c;<br> output diff, borrow;<br> wire w1,w2,w3;<br> xor gl (wl,a,b);<br> and g2 (w2,~a,b);<br> xor g3 (diff,wl,c);<br>
and (w3,c,~wl);<br> or g5 (borrow,w3,w2);<br> endmodule
## OUTPUT :
![image](https://github.com/JAYASHREEER/VLSI-EXPT-1/assets/166278992/d7dcf612-fd02-4476-b49d-1ea586c6f9ad)

## 8 BIT RIPPLE CARRY ADDER :
![image](https://github.com/JAYASHREEER/VLSI-EXPT-1/assets/166278992/6d83d485-1cb6-414b-afeb-88946f8b75e4)
## PROGRAM :
module FA(a, b, c, sum, carry);<br> input a, b, c;<br> output sum, carry;<br> assign sum=a ^ b ^ c;<br> assign carry=a & b|b & c|a & c;<br> endmodule<br>
module RCA(a, b, c, sum, carry);<br>input [7:0] a, b;<br>
input c; <br>output [7:0] sum;<br> output carry;<br> wire [6:0] w;<br>
FA f1(a[0], b[0], c, sum[0], w[0]);<br>
FA f2(a[1], b[1], w[0], sum[1], w[1]);<br>
FA f3(a[2], b[2], w[1], sum[2], w[2]);<br>
FA f4(a[3], b[3], w[2], sum[3], w[3]);<br>
FA f5(a[4], b[4], w[3], sum[4], w[4]);<br>
FA f6(a[5], b[5], w[4], sum[5], w[5]);<br>
FA f7(a[6], b[6], w[5], sum[6], w[6]);<br> FA f8(a[7], b[7], w[6], sum[7], carry);<br> endmodule
## OUTPUT :
![image](https://github.com/JAYASHREEER/VLSI-EXPT-1/assets/166278992/8f23ec30-ac97-4a79-8a04-68eac22e5d3f)

## RESULT :
       Thus simulate and synthesis Logic Gates, Adders and Subtractor using VIVADO
















