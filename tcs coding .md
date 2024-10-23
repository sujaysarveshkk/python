```python
def suf(a,k):
    n=0
    for i in a:
        n=n+i//k
        if n%k!=0:
            n+=1
    return n

a=[10,2,3,4,7]
k=4
print(suf(a,k))
```

    8
    


```python
def sumer(rad):
    return ((4//3)*(3.14)*rad**2)
```


```python
print(sumer(6))
```

    113.04
    


```python
def checkrange(num,low,higher):
       if num in range (low,higher+1):
           return True
           
       els
           print(False)
           
```


```python

print(checkrange(7,0,5))
```

    False
    None
    
count of upper case letters and lower casse letter

```python
def checkupper_lower(enterstring):
    lowercount=0
    uppercount=0
    for i in range (len(enterstring)):
        if enterstring[i].isupper():
            uppercount+=1
        elif enterstring[i].islower():
            lowercount+=1
    return lowercount,uppercount
print(checkupper_lower("THW hero"))

```

    (4, 3)
    


```python

```


```python
import string 
```


```python
def pangram(str,alfabets=string.ascii_lowercase):
    alfabets=set(alfabets)
    str=str.replace(" ","")
    str=str.lower()
    str=set(str)
    return str==alfabets
print(pangram("quick brown fox jumps over the lazy do"))
```

    False
    


```python
def display(input1,input2,input3):
    
    print(input1)
    print(input2)
    print(input3)
input1=['','','']
input2=['','','']
input3=['','','']
for i in input1:
display(input1,input2,input3)

```

    enter the value x
    

    ['', '', '']
    ['', 'x', '']
    ['', '', '']
    
creating a funtion to which get user input if not valid ask again with help of while loop and a.isdegit()

```python
def inputcheck():
    value=' '
    while value.isdigit()==False:
        value=input('enter the value ')
        if value.isdigit()==False:
            print('sorry you have enter the wrong value')
    return value
```


```python
inputcheck()
```

    enter the value  sujay
    

    sorry you have enter the wrong value
    

    enter the value  44
    




    '44'


now checking with both the range and isdigit() 

```python
def check1():
    value='wrint'
    acceptable_range=range(0,10)
    with_inrange=False
    while value.isdigit()==False or with_inrange==False:
        
        value=input('please enter the value ')
        # isdigit check
        if value.isdigit()==False:
            print('sorry you have entered a wrong or invalid value')
        # range check 
        if value.isdigit()==True:
            if int(value) in acceptable_range:
                with_inrange=True
            else:
                print('the value is not with in range ')
                with_inrange=False
                
    return int(value)
            
```


```python
check1()
```

    please enter the value  sujay
    

    sorry you have entered a wrong or invalid value
    

    please enter the value  100
    

    the value is not with in range 
    

    please enter the value  4
    




    4


creating a game where you can change the value in the list [1,2,3,]

```python
mylist=[1,2,3]
def display(mylist):
    print("these are the element present in the list ")
    print(mylist)

#selecting the position function 
def position(mylist):
    pos='' 
    while pos not in ['0','1','2']:
        pos=input("enter the position please")
        if pos not in ['0','1','2']:
            print("you have entered the wrong value ")
    return int(pos)
    
#creating the replace function 
def replace(mylist,pos):
    replacevalue=input("enter the value to replace")
    mylist[pos]=replacevalue
    return mylist

#creating the go on play function 
def goon():
    go=''
    while go not in ['Y','N']:
        go=input('enter the value yes are no as Y OR N')
        if go not in ['Y','N']:
            print('you have entered the wrong value')
    if go=='Y':
        return True
    else:
        return False

#main program with all this combined function 

go_on=True
mylist=[0,1,2]
while go_on:
    display(mylist)
    pos=position(mylist)
    mylist=replace(mylist,pos)
    display(mylist)
    go_on=goon()

    
```

    these are the element present in the list 
    [0, 1, 2]
    

    enter the position please two
    

    you have entered the wrong value 
    

    enter the position please 1
    enter the value to replace sujay
    

    these are the element present in the list 
    [0, 'sujay', 2]
    

    enter the value yes are no as Y OR N k
    

    you have entered the wrong value
    

    enter the value yes are no as Y OR N y
    

    you have entered the wrong value
    

    enter the value yes are no as Y OR N Y
    

    these are the element present in the list 
    [0, 'sujay', 2]
    

    enter the position please 0
    

    you have entered the wrong value 
    

    enter the position please 4
    

    you have entered the wrong value 
    

    enter the position please 0
    

    you have entered the wrong value 
    

    enter the position please 1
    enter the value to replace 2
    

    these are the element present in the list 
    [0, '2', 2]
    

    enter the value yes are no as Y OR N Y
    

    these are the element present in the list 
    [0, '2', 2]
    

    enter the position please 2
    enter the value to replace GU
    

    these are the element present in the list 
    [0, '2', 'GU']
    

    enter the value yes are no as Y OR N N
    


```python
#tic tac to game 
```


```python
from IPython.display import clear_output
```


```python
sam=['#',' ','x','x','o','o','x','o','x','o']
```


```python
def board(sam):
    clear_output()
    print(sam[7]+'|'+sam[8]+'|'+sam[9])
    print(sam[4]+'|'+sam[5]+'|'+sam[6])
    print(sam[1]+'|'+sam[2]+'|'+sam[3])


```


```python
board(sam)



```

    o|x|o
    o|o|x
     |x|x
    


```python
#creating the funcion for marker x or o
```


```python
def player():
    marker=0
    while marker !='x' and marker!='o':
        marker=input('ENTER THE MARKER VALUE PLEASE (x or o) ').lower()
    if marker == 'x':
        return('x','o')
    else:
        return('o','x')
     
    
```


```python
player()
```

    ENTER THE MARKER VALUE PLEASE (x or o)  x
    




    ('x', 'o')




```python
# Creating the funtion to get the marker  
```


```python
def position1(sam,marker,position):
    sam[position]=marker
```


```python
position1(sam,'y',4)

```


```python
board(sam)
```

    o|x|o
    y|o|x
     |x|x
    


```python
#creating the funtion to check winer 
```


```python
def winnercheck(sam,marker):
    return ((sam[7]==sam[8]==sam[9]==marker)or
            (sam[4]==sam[5]==sam[6]==marker)or
            (sam[1]==sam[2]==sam[3]==marker)or
            (sam[7]==sam[4]==sam[1]==marker)or
            (sam[8]==sam[5]==sam[2]==marker)or
            (sam[9]==sam[6]==sam[3]==marker)or
            (sam[7]==sam[5]==sam[3]==marker)or
            (sam[9]==sam[5]==sam[1]==marker))
```


```python
winnercheck(sam,'o')
```




    False




```python
#randam player choose function 
```


```python
import random
```


```python
def chooseplayer():
 
    flip=random.randint(0,1)
    if flip ==0:
        return 'player1'
    else:
        return 'player2'
```


```python
chooseplayer()
```




    'player2'




```python
#checking the space is available or not 
```


```python
def spacecheck(sam,position):
    return sam[position]==' '
```


```python
spacecheck(sam,1)
```




    True




```python
#check weather the game is tie or not by full space check
```


```python
def fullspacecheck(sam):
    for i in range(1,10):
        if spacecheck(sam,i):
            return False
    return True
        
```


```python
fullspacecheck(sam)
```




    False




```python
#creting a fuction that gets the user next position 
```


```python
def player_choice(board):
    position = 0
    
    while position not in [1,2,3,4,5,6,7,8,9] or not spacecheck(board, position):
        position = int(input('Choose your next position: (1-9) '))
        
    return position
```


```python
player_choice(sam)
```

    Choose your next position: (1-9)  1
    




    1




```python
#creating a replay funtion 
```


```python
def replay():
    play=input('YES IF YOU WANT TO PLAY AGAIN OR PRINT NO').lower()
    return play=='yes'
```


```python
replay()
```

    YES IF YOU WANT TO PLAY AGAIN OR PRINT NO yes
    




    True




```python
#main funtion call to combine all the funtion 
```


```python
print( "WELLCOME TO THE TIC TAC TO GAME ")
while True:
    sam=[' ']*10
    board(sam)
    player1_marker,player2_marker=player()
    turn=chooseplayer()
    print(turn+'will go first')
    play=input('do you want to play type : yes or no ')
    if play=='yes':
        gameon=True
    else :
        gameon=False

    while gameon:
        
            if turn=='player1':
                board(sam)
                position=player_choice(sam)
                position1(sam,player1_marker,position)
                
                
                if winnercheck(sam,player1_marker):
                    board(sam)
                    print('player 1 has won the game')
                    gameon=False
                else:
                    if fullspacecheck(sam):
                        board(sam)
                        print('the game is tie')
                        gameon=False
                    else:
                        turn='player2'
                    






            else:
                if turn=='player2':
                    board(sam)
                    position=player_choice(sam)
                    position1(sam,player2_marker,position)
                
                
                if winnercheck(sam,player2_marker):
                    board(sam)
                    print('player 2 has won the game')
                    gameon=False
                else:
                    
                    if fullspacecheck(sam):
                        board(sam)
                        print('the game is tie')
                        gameon=False
                    else:
                        turn='player1'
        
        
        

    




    if not replay():
        break
      
```

    x|x|x
     | |o
    o| | 
    player 2 has won the game
    


```python


```


```python

```
