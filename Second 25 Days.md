# Excersice 2: Kaun Banega Crorepati
Create a program capable of displaying questions to the user like KBC. 
Use List data type to store the questions and their correct answers.
Display the final amount the person is taking home after playing the game.

```python
q=['q1','q2','q3','q4','q5','q6','q7','q8','q9','q10','q11','q12','q13','q14','q15','q16']
a=['a1','a2','a3','a4','a5','a6','a7','a8','a9','a10','a11','a12','a13','a14','a15','a16']
p=[1000,2000,3000,5000,10000,20000,40000,80000,160000,320000,640000,1250000,2500000,5000000,10000000,70000000]
thr=p.index(int(input('Enter the threshold amount you want to earn: ')))
for i in range(len(q)):
	print(f'Write the answer of Question {q[i]} for Rs. {p[i]}. If you don\'t want to answer, press 0')
	ans=input()
	if ans=='0':
		print('You have quit the game')
		print('Your total winning so far is',p[i-1])
		break
		
	elif ans==a[i]:
		print(f'Correct Answer, You have won Rs. {p[i]}')
		if i==15:
			print('Congratulations, You have won the game')
	else:
		print('Yor answer is wrong')
		if(i>thr and i!=15):
			print(f'You won Rs. {p[thr]}')
		elif(i<=thr):
			print('You have won nothing')
		break
```

# String formatting in python
String formatting can be done in python using the format method.
```python
txt = "For only {price:.2f} dollars!"
print(txt.format(price = 49))
```
# f-strings in python
It is a new string formatting mechanism introduced by the PEP 498. It is also known as Literal String Interpolation or more commonly as F-strings (f character preceding the string literal). The primary focus of this mechanism is to make the interpolation easier.

When we prefix the string with the letter 'f', the string becomes the f-string itself. The f-string can be formatted in much same as the str.format() method. The f-string offers a convenient way to embed Python expression inside string literals for formatting.

## Example
```python
val = 'Geeks'  
print(f"{val}for{val} is a portal for {val}.")  
name = 'Tushar'  
age = 23  
print(f"Hello, My name is {name} and I'm {age} years old.")  
```
## Output:
```
Hello, My name is Tushar and I'm 23 years old.
```
In the above code, we have used the f-string to format the string. It evaluates at runtime; we can put all valid Python expressions in them.

We can use it in a single statement as well.
## Example
```python
print(f"{2 * 30})"  
```
## Output:
```
60
```
