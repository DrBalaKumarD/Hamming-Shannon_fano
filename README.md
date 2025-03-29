# Huffman-Shannon_fano
AIM:
To compute the Average Codeword Length, Entropy, Efficiency, Redundancy, and Variance for a discrete memoryless source using Huffman and Shannon-Fano coding based on the given probabilities and codeword lengths.

TOOLS REQUIRED:
python IDE with Numpy and Scipy.

PROGRAM:
import numpy as np
import math 
L  = 0
hs = 0
p = []
lk = []
n = int(input("Enter the number of Samples : "))
for i in range (n): 
    pr = float(input(f"Enter the probability of sample values {i + 1}: "))  
    p.append(pr)
for j in range (n): 
    l = float(input(f"Enter the length of the sample values {j + 1}: "))  
    lk.append(l)
for k in range (n):
    Avg1 = p[k] * lk[k]
    L = L + Avg1
for k in range (n):
    e = p[k] * math.log(1 / p[k], 2)
    hs = hs + e
hs = round(hs,3)
eff = hs / L
eff = round(eff,3)
red =  round(1 - eff,3) 
var = 0
for k in range(n):
    var1 = p[k] * (lk[k]-L)**2
    var = var + var1
var = round(var,3)
print()
print(f"Average Codeword Length is : {L}")
print(f"Entropy is : {hs}")
print(f"Efficiency is : {eff*100} %")
print(f"Redudancy is : {red}")
print(f"Variance is : {var}")
CALCULATION:
![image](https://github.com/user-attachments/assets/98ea7251-41f3-4ce7-b395-11be2b5af1c5)
![image](https://github.com/user-attachments/assets/063db0cf-8836-4d29-a086-e16554597ff1)
![image](https://github.com/user-attachments/assets/72b43b59-164a-4ccb-88df-71cbffe8e455)
![image](https://github.com/user-attachments/assets/66d4fa6a-7fe6-49a4-8aa6-e0e0a8ec3abe)
![image](https://github.com/user-attachments/assets/00f961ee-aef6-4ae6-9dad-3b28bfe431fa)
RESULT:
For the given probabilities 0.125,0.0625,0.25,0.0625,0.125,0.125,0.25

Average Codeword Length is : 2.625 Entropy is : 2.625 Efficiency is : 100.0 % Redudancy is : 0.0 Variance is : 0.484




