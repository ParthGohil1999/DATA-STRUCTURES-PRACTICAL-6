# DATA-STRUCTURES-PRACTICAL-6
# Write A Program to sort a list of elements. Give user the option to perform sorting using Insertion sort, Bubble sort or Selection


list1 = [10,20,30,40,50,60,70,80,90,100]
print("List = ",list1)
size = len(list1)
def binary_search(x):
    print("BINARY SEARCHING")
    low = 0
    high = len(list1) - 1
    mid = 0
    while low <= high: 
        mid = (high + low) // 2
        if list1[mid] < x: 
            low = mid + 1
        elif list1[mid] > x: 
            high = mid - 1
        else: 
            return mid 
    return "None it not in the list"



def linear_search(n):
	print("LINEAR SEARCHING")
	if n not in list1:
		print(n,"not in the list")
	else:
		for i in range(size):
			if list1[i]==n:
				print("index of ", n," is ",i)
				
n = input("Enter (L) for Linear search and  (B) for Binary search :")
if n=="L" or n=="l":
	y = int(input("Enter a no. from the given list1 "))
	linear_search(y)
elif n=="B" or n=="b":
	y = int(input("Enter a no. from the given list1 "))
	print("index of ",y," is ",binary_search(y))
else:
	print("Invalid input")
