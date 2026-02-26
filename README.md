#  Mean and variance of a discrete  distribution


# Aim : 

To find mean and variance of arrival of objects from the feeder using probability distribution


# Software required :  

Python and Visual components tool

# Theory:

The expectation or the mean of a discrete random variable is a weighted average of all possible
values of the random variable. The weights are the probabilities associated with the corresponding values. 
It is calculated as,

![image](https://user-images.githubusercontent.com/103921593/192938463-e34177f4-f188-48a0-bda2-8f6d1d660ed2.png)

The variance of a random variable shows the variability or the scatterings of the random variables.
It shows the distance of a random variable from its mean. It is calcualted as

![image](https://user-images.githubusercontent.com/103921593/192938695-99fedc01-34d5-4d36-84df-5880e766ed0c.png)


# Procedure :

1. Construct frequency distribution for the data

2. Find the  probability distribution from frequency distribution.

3. Calculate mean using 
   
   ![image](https://user-images.githubusercontent.com/103921593/192940431-03b81777-c54d-4286-b4f4-82dfe7666b4c.png)

4. Find  
   
      ![image](https://user-images.githubusercontent.com/103921593/192940255-2d9dd746-6875-4a6d-877b-6da6cdb96ab1.png)

5.  Calculate variance using 
  
      ![image](https://user-images.githubusercontent.com/103921593/192942852-913550a9-fabe-4a55-b956-0487b18bbd97.png)


# Experiment :

![image](https://user-images.githubusercontent.com/103921593/229993174-5b67e57e-3e01-4ac4-9f83-410a932b22bf.png)

# Program :
#### DEVELOPED BY : **AMSAVARADHAN M**<BR>Reg No : **212225230014**

### Declaring the value of n

```python
import numpy as np
n = int(input("Enter the value of n : "))
print("Value of n =", n)
```

### Getting the inputs

```python
InputVal = {}
for i in range(1, n+1):
    val = int(input(f"Enter the value no {i} : "))
    try:
        InputVal[val] += 1
    except:
        InputVal[val] = 1
print(f"{i} Values Collected Successfully")
```
### Finding Mean

``` python
mean = 0
for key, val in InputVal.items():
    mean += key*(val/n)
print(f"Mean = {mean:.3f}")
```
### Finding Variance

```python 
ex2 = 0
for key, val in InputVal.items():
    ex2 += ((key**2) * val/n)
var = ex2 - mean**2
print(f"Variance : {var:.3f}")
```
### Finding Standard Deviation

```python
from math import sqrt
sdtDeviation = sqrt(var)
print(f"Standard Deviation = {sdtDeviation:.3f}")
```

# Output : 
<img width="490" height="170" alt="image" src="https://github.com/user-attachments/assets/b46d15e1-6735-4afb-94ab-8c7e061cc2a6" />
<img width="490" height="256" alt="image-1" src="https://github.com/user-attachments/assets/f9d63a4c-88f2-4249-a23e-dd5ce8b426a1" />
<img width="491" height="175" alt="image-2" src="https://github.com/user-attachments/assets/eb312ade-0c9f-4f70-b8c6-ab4d2de3eb7c" />
<img width="490" height="201" alt="image-3" src="https://github.com/user-attachments/assets/e7c91dc2-2c36-44b5-ae72-7c412a7e936c" />
<img width="487" height="164" alt="image-4" src="https://github.com/user-attachments/assets/6aca3573-a901-411c-81f8-6b856e5353b1" />


# Results :
The mean and variance of arrivals of objects from feeder using probability distribution are calculated.

