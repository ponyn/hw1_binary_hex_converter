# hw1_binary_hex_converter
import math
decimal_number=input("please enter number in decimal")
decimal_number=int(decimal_number)
power7=decimal_number//(2**7)
power6=(decimal_number % (2**7))//(2**6)
power5=(decimal_number % (2**6))//(2**5)
power4=(decimal_number % (2**5))//(2**4)
power3=(decimal_number % (2**4))//(2**3)
power2=(decimal_number % (2**3))//(2**2)
power1=(decimal_number % (2**2))//(2**1)
power0=(decimal_number % (2**1))
binary_number=power7*(10**7)+power6*(10**6)+power5*(10**5)+power4*(10**4)+power3*(10**3)+power2*(10**2)+power1*(10)+power0
print(binary_number)
hexadecimal_number_1=power7*2*2*2+power6*2*2+power5*2+power4
hexadecimal_number_2=power3*2*2*2+power2*2*2+power1*2+power0
global hexadecimal_number
hexadecimal_dictionary={10:'A',11:'B',12:'C',13:'D',14:'E',15:'F'}
if hexadecimal_number_1<10 and hexadecimal_number_2<10:
  print(hexadecimal_number_1*10+hexadecimal_number_2)
elif hexadecimal_number_1<10 and hexadecimal_number_1>0:
  print(hexadecimal_number_1,hexadecimal_dictionary[hexadecimal_number_2])
elif hexadecimal_number_2<10:
  print(hexadecimal_dictionary[hexadecimal_number_1],hexadecimal_number_2)
elif hexadecimal_number_1>=10 and hexadecimal_number_2>=10:
  print(hexadecimal_dictionary[hexadecimal_number_1],hexadecimal_dictionary[hexadecimal_number_2])
else:
  print(hexadecimal_dictionary[hexadecimal_number_2])
