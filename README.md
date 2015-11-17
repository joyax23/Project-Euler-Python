# Project-Euler-Python
Easter Joy Trocio Codes


'''Problem Number 1'''
l=[]
for i in range(1000):
    if i%3== 0 or i%5==0:
        l.append(i)
b=list(set(l))
print sum(b)

###########################
'''Problem Number 2'''
f=[1, 2, 3, 5, 8, 13, 21, 34, 55, 89]

#Create a list of fibonacci sequence until 4000000
while f[len(f)-1]<4000000:
    n=f[len(f)-2]+f[len(f)-1]
    f.append(n)

f.pop(len(f)-1)
    
#check if even
A=[]
for i in f:
    if i%2==0:
        A.append(i)
    
sum(A)

###########################

'''Problem Number 3'''

#Check if a number is a factor of 600851475143 
fact=[]
n=600851475143
p=int(sqrt(n))+1
for i in range(2,p):
    if n%i==0:
        fact.append(i)  
     
#IsPrime

def isPrime(n):
    for i in range(2,int(n**0.5)+1):
        if n%i==0:
            return 1

    return 1

fact.reverse()

for i in fact:   
    if isPrime(i)==1:
        print i
        break

###########################

''''Problem 4'''

def ReverseNumber(n, partial=0):
    if n == 0:
        return partial
    print ReverseNumber(n / 10),partial
    return ReverseNumber(n / 10, partial * 10 + n % 10)

A=range(700,999)
B=range(700,999)
A.reverse()
B.reverse()
for i in A:
    for j in B:
        a=i*j
        if a == ReverseNumber(a):
            print a
            break

########################### 

''''Problem 5'''


# Python Program to find the factors of a number

# define a function
def primes(n):
    primfac = []
    d = 2
    while d*d <= n:
        while (n % d) == 0:
            primfac.append(d)  # supposing you want multiple factors repeated
            n //= d
        d += 1
    if n > 1:
       primfac.append(n)
    return primfac



def factor(n):
    fact=[]
    p=n/2+1
    for i in range(2,p):
        if n%i==0:
            fact.append(i)  
    return fact
F=[]
for i in range(2,11):
        F.append(primes(i))
#Get the Prime factors too

###########################

'''Problem Number 6''' 

sum(i**2 for i in range(101))-sum(range(101))**2

               
                              
'''Problem Number 07''' 
n=0
a=2
while n !=10001:
    if isPrime(a)==1:
        n=n+1
        A.append(a)
    a=a+1
    
    
    
    
    
'''Problem Number 9'''

                                                                                       
                                                                                                                                                                              
 ###########################                                                                                                                                                                                                                                                                                                                                          
                  
'''Problem Number 10'''   
A=[]          
for i in range(10):
    if isPrime(i)==1:
        A.append(i)

n=0
a=2
while n !=2000000:
    if isPrime(a)==1:
        n=n+1
        A.append(a)
    a=a+1
                   
 ############################
                       
# Euler 10
# http://projecteuler.net/index.php?section=problems&id=10
# The sum of the primes below 10 is 2 + 3 + 5 + 7 = 17.
# Find the sum of all the primes below two million.

def sum_primes(limit):
    primes = []
    for n in xrange(2, limit+1):
        # try dividing n with all primes less than sqrt(n):
        for p in primes:
            if n % p == 0: break     # if p divides n, stop the search
            if n < p*p:
               primes.append(n)      # if p > sqrt(n), mark n as prime and stop search
               break
        else: primes.append(n)       # fallback: we actually only get here for n == 2
    return sum(primes)

'''Problem Number 12'''

def factor(n):
    fact=[]
    for i in range(2,n+1):
        if n%i==0:
            fact.append(i)  
    return fact

n=117440512
while len(factor(n))<=500:
    m=max(factor(n))
    n=n+m
    print n, len(factor(n))
               

                  
'''Problem Number 16'''   

N=[int(i) for i in str(2**1000)]
sum(N)
