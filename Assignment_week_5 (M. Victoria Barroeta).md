
# Assignment for week 5

Use the following table to provide us with

|name| exam number|
|----|----|
|M. Victoria Barroeta| Snr. 2001821, ANR: 933733|


```python

```

In the lecture we considered a two period bargaining model. In this assignment we are going to extend this to 3 periods.

Pay attention to what you do here. The python part of the final assignment will be the extension to $n$ bargaining periods; but let us not worry about this yet.

We need the following library:


```python
import numpy as np
```


```python

```


```python

```

As we are looking at more periods here, we need a finer grid of offers. We want all offers between 0.0 and 10.0 (including 10.0) with step 0.1 between offers.

**1)** Define the list `offers` using `np.arrange`:


```python

```


```python
min_offer = 0.0
max_offer = 10.0
step = 0.1
offers = np.arange(min_offer,max_offer+0.1,0.1)

```

**2)** Copy the function `accept_offer` from the lecture:


```python
def accept_offer(offer,your_outside_option):
    accept = (offer >= your_outside_option)
    return accept
```

**3)** Copy the function `make_offer` from the lecture:


```python
def make_offer(your_outside_option,other_outside_option):
    profits = [(max_offer-offer)*accept_offer(offer,other_outside_option) for offer in offers]
    max_profit = max(profits)
    max_index = profits.index(max_profit)
    if max_profit >= your_outside_option:
        your_offer = offers[max_index]
        your_profit = max_offer-offers[max_index]
        other_profit = offers[max_index]
    else:
        your_offer = -1 # no offer is made
        your_profit = your_outside_option
        other_profit = other_outside_option
    return your_offer, your_profit, other_profit
```

Pay attention to what `make_offer` returns and in which order. You need this below.

In this assignment, we are looking at the three period bargaining problem. We want to use the function `make_offer` to keep track of the outside options without defining a new dictionary `outside_options` (as we did in the lecture).

As in the lecture, we will use backward induction to solve this. That is, we first consider what happens in period 3 --in case the offers made in periods 1 and 2 are rejected. Once we know what will happen in period 3, we can move back to period 2 and then to period 1.

To do this, we create a dictionary `offer`. 

**4)** Explain what the following code does (e.g. what is `offer[4]`?).


```python
delta = 0.9
offer = {}
offer[4] = [0,0,0]
offer[3] = make_offer(delta*offer[4][2],delta*offer[4][1])
```

give your explanation here: "offer" describes the offer made and profits made by both participants each round. Each round player 1 tries to get a higher profit by changing the offer, thus leading to different profits for both players. In period 4 player 2 is no longer willing to accept player 1's offers, thus negotiations break down and there are no profits made.

**5)** Using the logic above, define `offer[2]` and `offer[1]`:


```python
offer[2] = make_offer(delta*offer[3][2],delta*offer[3][1])
offer[1] = make_offer(delta*offer[2][2],delta*offer[2][1])
```

**6)** What are the payoffs for players 1 and 2 in a three period version of the bargaining model in the lecture?

**Player1:** 
Period 1: 9.0999999999999996
Period 2: 1.0

**Player2:**
Period 1: 0.90000000000000002
Period 2: 9.0

**7)** In which period will the players reach an agreement?

They will reach to an agreement in Period 1


```python
offer
```




    {1: (0.90000000000000002, 9.0999999999999996, 0.90000000000000002),
     2: (9.0, 1.0, 9.0),
     3: (0.0, 10.0, 0.0),
     4: [0, 0, 0]}



6) 
