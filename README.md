print("Black Jack")
import random
Player1=[]
Computer1=[]
def Black_Jack(Player,Computer):
    if Computer == 0 or Player ==0:
        False
        if Computer == 0:
            print("Player Won!!!")
        else:
            print("Computer Won!!!")
    Player = 2000
    Computer = 2000 
    BidBox=0 
    while True:    
        Cards=[1,2,3,4,5,6,7,8,9,10,10,10,10,11]
        
        BidBox=0
        
        for _ in range(2):
            card=random.choices(Cards)
            card.append(random.choice(Cards))
        Player1 = card
        print(Player1)
        Player-=100  
        BidBox+=100
        for _ in range(2):
            card1=random.choices(Cards)
        Computer-100    
        BidBox+100
        Computer1 =card1    
        print(f"Computer s hand  {Computer1} and ? ")
        q=input("Would You want to take another one? y or no : ")
        if q == "y":
            Player-=100  
            BidBox+=100 
            card.append(random.choice(Cards)) 
            print(Player1)
        elif q== "n":
            Player1=card
            print(Player1)
        else:
            break
        for _ in range(2):
            card1.append(random.choice(Cards))
            if sum(Computer1)<11:
                Computer-=100    
                BidBox+=100
                for _ in range(2):
                    card1.append(random.choice(Cards))
            else:
                Computer1=card1
        if sum(Player1)==21 and sum(Computer1)== 21:
            BidBox-=200
            Player+=100
            Computer+100
            print("Draw")
        elif  sum(Player1)>21 and sum(Computer1)== 21:
            BidBox-=200
            Computer+=100
            print("Computer1 is won")
        elif sum(Player1)>21 and sum(Computer1)< 21:  
            BidBox-=100
            Computer+=100
            print("Computer1 is won")
        elif  sum(Player1)<21 and sum(Computer1)<21:
            if sum(Player1)> sum(Computer1):
                BidBox-=200
                Player+=100
                print("Player1 is won")
            else:
                BidBox-=100
                Computer+=100
                print("Computer1 is won")
        elif  sum(Player1)==21 and sum(Computer1)<21: 
            BidBox-=200
            Player+=100
            print("Player1 is won")
        elif  sum(Player1)==21 and sum(Computer1)>21:  
            BidBox-=200
            Player+=100
            print("Player1 is won")
        elif  sum(Player1)>21 and sum(Computer1)>21:
            BidBox-=200
            Player+=100
            Computer+100
            print("Draw")
        else:
            BidBox-=200
            Player+=100
            Computer+=100
            print("Draw")
    if Computer==0:
        False
         
            
Black_Jack(Player1,Computer1)            