# Health-Management-System-in-Python
It is a basic code and easy to understand

import datetime
def gettime():
    return datetime.datetime.now()

try:

	client_list={1:"Harry",2:"Gautam",3:"Sara"}
	log_list={1:"add",2:"retreive"}
	work_list={1:"diet",2:"exercise"}
	while True:

		for key,value in client_list.items():
			print("press",key,"for",value,"\n",end="")

		client_number=int(input())
		print()
		print("selected client is",client_list[client_number])
		print()

		for key,value in log_list.items():
			print("press",key,"to",value,"\n",end="")
		log_number=int(input())
		print()
		for key,value in work_list.items():
				print("press",key,"for",value,"\n",end="")
		work_number=int(input())
		print()

		if log_number==1:
			
			if client_number==1:
				if work_number==1:
					
					
					while True:
						diet1=input("enter what did you just eat?")
						f=open("Harrydiet.txt","a")
						f.write(str([str(gettime())]) + ": " + diet1 + "\n")
					
							
						print("succesfully updated")
						print()
						f.close()
						print("Do you want to add mmore y/n")
						a=input()
						if a=="y":
							continue
						elif a=="n":
							break
						else:
							print("enter a valid number")
							break

				elif work_number==2:
					exercise1=input("enter what you did")
					f=open("Harryexercise.txt","a")
					f.write(str([str(gettime())]) + ": " + exercise1 + "\n")
					print("succesfully updated")
					f.close()
				else:
					print("please enter valid operation")
			elif client_number==2:
				if work_number==1:
					diet2=input("enter what did you just eat?")
					f=open("Gautamdiet.txt","a")
					f.write(str([str(gettime())]) + ": " + diet2 + "\n")
					print("succesfully updated")
					f.close()
				elif work_number==2:
					exercise2=input("enter what you did")
					f=open("Gautamexercise.txt","a")
					f.write(str([str(gettime())]) + ": " + exercise1 + "\n")
					print("succesfully updated")
					f.close()
				else:
					print("please enter valid operation")
			elif client_number==3:
				if work_number==1:
					diet3=input("enter what did you just eat?")
					f=open("Saradiet.txt","a")
					f.write(str([str(gettime())]) + ": " + diet3 + "\n")
					print("succesfully updated")
					f.close()
				elif work_number==2:
					exercise3=input("enter what you did")
					f=open("Saraexercise.txt","a")
					f.write(str([str(gettime())]) + ": " + exercise1 + "\n")
					print("succesfully updated")
					f.close()
				else:
					print("please enter valid operation")
			else:
				print("please enter valid client_number and try again")


		elif log_number==2:
			
			
			if client_number==1:
				if work_number==1:
					f=open("Harrydiet.txt","rt")
					print("Harry's diet :")
					content=f.read()
					print(content)
					f.close()
				elif work_number==2:
					f=open("Harryexercise.txt","rt")
					print("Harry's exercise :")
					content=f.read()
					print(content)
					f.close()
				else:
					print("please enter valid operation")
			if client_number==2:
				if work_number==1:
					f=open("Gautamdiet.txt","rt")
					print("Gautam's diet :")
					content=f.read()
					print(content)
					f.close()
				elif work_number==2:
					f=open("Gautamexercise.txt","rt")
					print("Gautam's exercise :")
					content=f.read()
					print(content)
					f.close()
				else:
					print("please enter valid operation")
			if client_number==3:
				if work_number==1:
					f=open("Saradiet.txt","rt")
					print("Sara's diet :")
					content=f.read()
					print(content)
					f.close()
				elif work_number==2:
					f=open("Saraexercise.txt","rt")
					print("Sara's exercise :")
					content=f.read()
					print(content)
					f.close()
				else:
					print("please enter valid operation")
				

		else:
			print("please enter valid operation")

		print("Do you want to repeat y/n")
		a=input()
		if a=="y":
			continue
		elif a=="n":
			break
		else:
			break
except :
	print("try again")

