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
