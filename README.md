1....................................
Num=int(input("Enter the range of numbers \n"))
list_1=[]
for j in range(1,Num+1):
    user_choice =input("Enter the numbers \n")
    list_1.append(user_choice)
    tup=tuple(list_1)
print("The Maximum number is {} \n Minimum number is {}".format(max(tup),min(tup)))    


input/output

Enter the range of numbers 
3
Enter the numbers 
1
Enter the numbers 
2
Enter the numbers 
3
The Maximum number is 3 
 Minimum number is 1

2.......................................
odd={1:"one",3:"three",5:"five",7:"seven",9:"nine"} 
print("keys are",(list(odd.keys()))) 
print("values are",(list(odd.values())))
print("items are",(list(odd.items()))) 
print("length of dictionary is ",(len(odd)))
if 7 in odd:
     print('Number is available')
else:
     print("not found")
if 2 in odd:
     print('Number is available')
else:
     print("not found")        
print(odd[9]) 
odd.pop(9)
print(odd)

Input/Output

keys are [1, 3, 5, 7, 9]
values are ['one', 'three', 'five', 'seven', 'nine']
items are [(1, 'one'), (3, 'three'), (5, 'five'), (7, 'seven'), (9, 'nine')]
length of dictionary is  5
Number is available
not found
nine
{1: 'one', 3: 'three', 5: 'five', 7: 'seven'}


3.........................................

employee_data={}  
i=True  
while(i):
    name=input("Enter the name \n")
    print("enter employee salary ")
    salary=int(input())
    employee_data.setdefault(name,salary)
    print("the employee data is",employee_data) 
    print(" continue :(y/n)")
    n = (input().upper())
    while n !="Y" and n!="N":
        n=(input("invalid input enter again").upper()) 
    if n!="Y": 
        break 
    else: 
        continue

Input/Output

Enter the name 
ram
enter employee salary 
4000
the employee data is {'ram': 4000}
 continue :(y/n)
n
4...................................................

dict1={}
print("enter the string") 
str1=input()
for i in str1: 
    count1=str1.count(i)
    dict1.setdefault(i,count1)
print(dict1)dict1={}
print("enter the string") 
str1=input()
for i in str1: 
    count1=str1.count(i)
    dict1.setdefault(i,count1)
print(dict1)



Input/Output

enter the string
rohit singh sagar
{'r': 2, 'o': 1, 'h': 2, 'i': 2, 't': 1, ' ': 2, 's': 2, 'n': 1, 'g': 2, 'a': 2}


5..........................................................

print("enter a number :") 
num=(input())
dict1={1:"one",2:"two",3:"three",4:"four",5:"five",6:"six",7:"seven",8:"eight",9:"nine",0:"zero"} 
def converter(n): 
    for i in n: 
        if int(i) in dict1.keys():
            print(dict1[int(i)].title(),end=" ")
converter(num)



Input/Output

enter a number :
466
Four Six Six 

6..............................................................

stdname=[]
n=int(input("enter the number of names: "))
for i in range(0,n): 
    print("enter a name : ") 
    stdname.append(input())
tup=tuple(stdname)

find=input("enter a name to find :") 
if find in tup: 
    print(find + " is present")
else: 
    print("not present")



Input/Output


enter the number of names: 3
enter a name : 
ram 
enter a name : 
shyam
enter a name : 
rohit
enter a name to find :ravi
not present


7..............................................................

phone_diary={}  
i=True 
while(i):
    name=input("Enter the Name \n") 
    number =int(input("Enter Phone Number \n"))
    phone_diary[name]=number
    n = (input(" continue :(y/n)").upper()) 
    while n !="Y" and n!="N":
        n=(input("invalid input enter again").upper())
    if n!="Y": 
        break 
    else:
        continue  
def display_phonediary(n):
    for i,j in n.items():
        print("Name: "+i,"phone number:",j)     
def update_phonediary(n): 
    print("enter a new name: ")
    name=input() 
    print("enter phone number ")
    number =int(input())
    n[name]=number        
def del_entry(n): 
    print("enter a name to delete: ") 
    name=input()
    n.pop(name) 
def modify_entry(n): 
    print("enter a name to be modified : ") 
    name=input() 
    print("enter a new number: ")
    number=int(input())
    n[name]=number 
def find(n): 
    print("enter a name to find: ")
    name=input() 
    if name in n.keys():
        print(name + " is present")
    else: 
        print(name+" not present")
def sort_phone_diary(n): 
    new_phone_diary=sorted(n.items()) 
    print(dict(new_phone_diary))
print("choose any of following operations below")
print( """"AA" to Display the name and phone number of all your friends
        "BB" to Add a new entry in phone diary and display the modified dictionary 
        "CC" to Delete a particular friend from the dictionary 
        "DD" to Modify the phone number of an existing friend 
        "EE" to Check if a friend is present in the dictionary or not 
        "FF" to Display the dictionary in sorted order of names""")        
op=input().upper() 
if op=="AA":   
    display_phonediary(phone_diary)
elif op == "BB": 
    update_phonediary(phone_diary) 
    display_phonediary(phone_diary) 
elif op == "DD":
    modify_entry(phone_diary) 
    display_phonediary(phone_diary)
elif op == "CC":
    del_entry(phone_diary) 
    display_phonediary()
elif op == "EE": 
    find(phone_diary) 
elif op == "FF":
    sort_phone_diary(phone_diary) 


Input/Output   

Enter the Name 
rohit
Enter Phone Number 
9971643265
 continue :(y/n)n
choose any of following operations below
"AA" to Display the name and phone number of all your friends
        "BB" to Add a new entry in phone diary and display the modified dictionary 
        "CC" to Delete a particular friend from the dictionary 
        "DD" to Modify the phone number of an existing friend 
        "EE" to Check if a friend is present in the dictionary or not 
        "FF" to Display the dictionary in sorted order of names
EE
enter a name to find: 
rohit
rohit is present


8.............................................................................


list_operations=[1,2,3,4,5,6]
print(""" choose the following operations:
"AA" to Append an element 
"BB" to Insert an element
"CC" to Append a list to the given list 
"DD" to Modify an existing element 
"EE" to Delete an existing element from its position 
"FF" to Delete an existing element with a given value
"GG" to Sort the list in ascending order 
"HH" to Sort the list in descending order 
"II" to Display the list """)
def display_list(n): 
    print(n) 
def appnd_element(n):
    print("enter element to append")
    inp=input()
    n.append(inp)
def insert_element(n):
    print("enter and element to insert")
    key=input() 
    pos=int(input())
    n.insert(pos,key)
def appnd_list_list(n): 
    print("enter elements of the second list ")
    list2=[input() for i in range(10)] 
    n.append(list2)    
def modify_existing_element(n):
    print("enter element to be modified") 
    inp=input() 
    print("enter the new value ")
    new_val=input() 
    pos=n.index(inp)
    n[pos]=new_val 
def Delete_existing_element(n): 
    print("enter element to be deleted") 
    inp = input()
    n.remove(inp)    
def Delete_existing_element_position(n): 
    print("enter the position ") 
    inp = int(input())
    n.pop(inp)    
def sort_ascending(n): 
    n.sort() 
def sort_descending(n): 
    n.sort(reverse=True) 
select=input("enter your selection :").upper()
if select =="AA":
    appnd_element(list_operations) 
    display_list(list_operations) 
elif select == "BB": 
    insert_element(list_operations) 
    display_list(list_operations)
elif select == "CC":
    modify_existing_element(list_operations) 
elif select == "DD": 
    modify_existing_element(list_operations)
    display_list(list_operations) 
elif select == "EE":
    Delete_existing_element(list_operations) 
    display_list(list_operations) 
elif select == "FF":
    Delete_existing_element_position(list_operations)    
    display_list(list_operations)
elif select == "GG":
    sort_ascending(list_operations) 
    display_list(list_operations) 
elif select == "HH":
    sort_descending(list_operations)
    display_list(list_operations) 
elif select=="II":
    display_list(list_operations)


Input/Output

choose the following operations:
"AA" to Append an element 
"BB" to Insert an element
"CC" to Append a list to the given list 
"DD" to Modify an existing element 
"EE" to Delete an existing element from its position 
"FF" to Delete an existing element with a given value
"GG" to Sort the list in ascending order 
"HH" to Sort the list in descending order 
"II" to Display the list 
enter your selection :AA
enter element to append
4
[1, 2, 3, 4, 5, 6, '4']



9...............................................

set1 = {10, 20, 30, 40, 50} 
set2 = {30, 40, 50, 60, 70} 
print(set1.intersection(set2))


Input/Output
{40, 50, 30}
10.............................................


str1=input("Enter the string \n")
for i in str1:
    count1=str1.count(i) 
print(count1==1)


Input/Output

Enter the string 
smit
True



