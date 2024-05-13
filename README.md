Heres a systematic strategy we'll apply for solving problems:
1. State the problem clearly. Identify the input and output format
2. Come up with some example inputs and outputs. Try to cover all edge cases.
3. come up with a correct solution for the problem. State it in plain English.
4. Implement the solution and  test it using example inputs. Fix bugs, if any.
5. Analyze the algorithm's complexity and identify inefficiencies, if any.
6. Apply the right technique to overcome the inefficiency. Repeat steps 3 to 6.


Applying the right technique is where the knowledge of common data structures and algorithms come in handy.



# Problem 1
<i>Alice has some cards with numbers written on them.
She arranges the cards in decreasing order, and lays them
out face down in a sequence on a table. She challenges Bob
to pick out the card conatining a given number by turning
over as few cards as possible. Write a function to help
bob locate the card</i>

## Solution

# 1. State the problem clearly. Identify the input and output formats.

You will often encounter detailed word problems in coding challenges and interviews. The first step is to state the problem clearly and precisely in abstract terms.

In this case, for instance, we can represent the sequence of cards as a list of numbers. Turning over specific card is equivalent to accessing the value of the number at the corresponding position the list.

    sorted_list = [13,11,12,7,4,3,1,0]
                    0  1  2 3 4 5 6 7
    Queried Numbers = 7
    Answer = list[3]
The problem can now be stated as follows:

## Statement
<i> We need to write a program to find the position of a given number in a list of numbers arranged in decreasing order.
We also need to minimize the number of times we access elements from the list.</i>

## Input
1. cards: A list of numbers sorted in decreasing order. EG: [13,11,10,7,4,3,1]
2. query: A number, whose position in the array is to be determined. EG: 7

## Output
1. position: The position of query in the list cards. EG. 3 in the above case (counting from 0)

Algorithm using Linear Search:
1. Create a variable position with the value 2
2. Check whether the number at index position in card equals query.
3. If it does, position is the answer and can be returned from the function.
4. If not, increment the value of position by 1, and repeat steps 2 to 5 till we reach the last position.
5. if the number was not found return -1.

