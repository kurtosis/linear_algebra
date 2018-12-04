# Markov Processes!

Let's say I have an object that can be in one of two states: state A or state B.
After each "period of time" the object can change to a new state. (We're a little vague on what 
the "period of time" is but we'll see in the examples below)

For example, let's say the "object" is a person and the two states are happy and sad. Also people are more
likely to stay happy if they are happy, or stay sad if they are sad
Suppose the numbers are:
- If person is happy today there is an   80% chance they will be happy tomorrow.
- If person is sad today there is only a 30% chance they will be happy tomorrow.

Or another example, say every day I have to choose sushi or tacos for lunch. But I like to mix it up from
day to day so:
- If I ate sushi today there is a 20% chance I will eat sushi tomorrow.
- If I ate tacos today there is a 90% chance I will eat sushi tomorrow.

Even flipping a coin is a markov process:
- If the last flip was heads there is a 50% chance the next flip will be heads.
- If the last flip was tails there is a 50% chance the next flip will be heads.

(of course here it doesn't really matter what the last flip was, the next flip is always 50/50)

Finally we can talk about the employment rate. Suppose:
- If a person is employed this year, there is a 90% chance they will be employed next year.
- If a person is unemployed this year, there is a 60% chance they will be employed next year.

And let's say that these probabilities hold true for every person, every year.
Then if we wait many years, we will eventually hit a point where the unemployment rate stays
constant. That means the number of employed people who lose their jobs every year is exactly
balanced by the number of unemployed people who find a job. What is this equilibrium unemployment rate?
If N is the # of people employed and M is the # of people unemployed then:
- 0.1*N people lose their job every year (employed --> unemployed)
- 0.6*M people find a job every year (unemployed --> employed)

If these numbers are balanced then:

0.1\*N = 0.6\*M

N = 6*M

So the percent of people who are unemployed is M/(M+N) = M/(M+6*M) = 1/7 = 14.3%.

We can write this as a "transition matrix"
A = [[0.9, 0.6],
     [0.1, 0.4]]

If 
- x = [\% of people employed this year, \% of people unemployed this year]

then 
- A\*x = [\% of people employed NEXT year, \% of people unemployed NEXT year]

In the question above we are trying to find the "equilibrium" value of x such that A\*x=x.
In other words...the eigenvector with eigenvalue = 1 !




# Midterm Questions

A basis of R^3 in which every vector IN THE BASIS verifies 2x+y+z = 1 (hint: notice the “1”)

we want a basis B. B has three linearly independent vectors.
B = [basis_vector1, basis_vector2, basis_vector3]

basis_vector1 = (x1, y1, z1)
basis_vector2 = (x2, y2, z2)
basis_vector3 = (x3, y3, z3)

First vector
2*x1 + y1 + z1 = 1
(1/2, 0, 0)


Second vector
2*x2 + y2 + z2 = 1

---------

e1 is a VECTOR
e1 is the vector (1,0,0)

e2 is a VECTOR
e2 is the vector (0,1,0)

e3 is a VECTOR
e3 is the vector (0,0,1)

[e1, e2, e3] is a set of three vectors that is a basis of R^3

[1/2*e1, e2, e3] is ALSO a basis of R^3

[-e1, -e2, -e3] is ALSO a basis of R^3

[100*e1, 5*e2, -20*e3] is ALSO a basis of R^3


[e1+e2, e2+e3, e3-e1] is NOT a basis of R^3

----------

What is this?
[e1+e2, e2+e3, e3-e1]
first vector: (1,1,0)
second vector: (0,1,1)
third vector: (-1,0,1)
Is this a basis? NO!

----------

This is a basis:
[e1+e2, e2+e3, ?]
first vector: (1,1,0)
second vector: (0,1,1)
third vector: (1,0,1)


All these statements are equivalent for a set of three vectors in R^3:
- the vectors span R^3 (= they are a basis)
- the vectors are linearly independent
- 0 is not an eigenvalue
- the determinant != 0
(the last because determinant = Prod(lambda_i) = lambda_1*lambda_2*lambda_3)

