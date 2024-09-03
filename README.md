# Phone-book
#Basic Phone Book in which you can add, delete, search contacts.

def add(phonebook):
    name=input("Enter name to add in contacts:")
    num=int(input("Enter Phone no.-"))
    phonebook[name]=num
    print(f"\n{name} is added to contacts\n")
    control()
    
def veiw(phonebook):
      print("\n")
      for name, phone in phonebook.items():
            print(f"Name: {name}, Phone Number: {phone}")
      print("\n")      
      control()  
      
def search(phonebook):
    name=input("Enter name to be search:")
    if name in phonebook:
        print(f"\nName: {name}, Phone Number: {phonebook[name]}\n")
    else:
        print(f"\n{name} is not present\n")
    control()    

def delete(phonebook):
    name=input("Enter name to delete:")
    if name in phonebook:
        del phonebook[name]
        print(f"\n{name} is deleted succesfully\n")
    else:
        print(f"\n{name} is not present\n")
        
    control()
    
def control():
   
    print("Phone Book Menu/-")
    print(">Enter 1 to add contact")
    print(">Enter 2 to veiw contacts")
    print(">Enter 3 to search contacts")
    print(">Enter 4 to delete contact")
    print(">Enter 5 to Exit")
    n=int(input("Enter Choice:-"))
    
    if n==1:
       add(phonebook)
    elif n==2:
         veiw(phonebook)
    elif n==3:
        search(phonebook)
    elif n==4:
        delete(phonebook)
    elif n==5:
        print("\n>Exit Phonebook Succesfully")
    
phonebook={}
control()
