def  countSetBits(n): 
    count = 0
    while (n): 
        count += n & 1
        n >>= 1
    return count 
  
  
# Program to find 1 in binary number in an Integer */ 
i = 9
print(countSetBits(i)) 
