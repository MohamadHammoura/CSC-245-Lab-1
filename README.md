# CSC-245-Lab-1

# Create a rank 2 (2D) array that resembles the matrix below.
 [[11 12 13 14]
 [15 16 17 18]]

my_array = np.array([[11, 12, 13, 14],
                     [15, 16, 17, 18]])
print(my_array)


# Create an array with 4 rows and 3 columns of zeros. Your results should look as below:
[[0. 0. 0.]
 [0. 0. 0.]
 [0. 0. 0.]
 [0. 0. 0.]]



my_array = np.zeros((4,3))

print(my_array)


# Create an array of ones that has 3 rows and 4 columns. Your results should look as below:
[[1. 1. 1. 1.]
[1. 1. 1. 1.]
[1. 1. 1. 1.]]

my_array = np.ones((3,4))
print(my_array)

# Create an array containing integers 4 to 13 inclusive. Your results should look as below:
[4 5 6 7 8 9 10 11 12 13]

my_array = np.arange(4,14)
print(my_array)

#  Create an array containing
[0., 1.5, 3., 4.5]

my_array = np.array([0 , 1.5 , 3, 4.5])
print(my_array)

# Create a 2 by 2 array containing '4' in each position. Your results should look like this:
[[4 4]
 [4 4]]

my_array = np.array([[4, 4],
                     [4, 4]])
print(my_array)

#  Create 2 matrices:

i. Identity matrix of size 4
[[1. 0. 0. 0.]
 [0. 1. 0. 0.]
 [0. 0. 1. 0.]
 [0. 0. 0. 1.]]
ii. Diagonal matrix with [10,12] as the diagonals 
[[10  0]
 [ 0 12]]


identity_matrix = np.eye(4)
print("Identity matrix of size 4:")
print(identity_matrix)

diagonal_matrix = np.diag([10, 12])
print("\n diagonal matrix:")
print(diagonal_matrix)


# Create a 3 by 3 array with random floats in [0, 10]. Your answer may be different because it is random but it should look something like this:
[[6.3685612  0.61720883 8.93157783]
 [3.69927617 5.79879583 7.62145626]
 [7.21895112 4.02011535 4.48844787]]

random_array = np.random.random((3, 3)) * 10

print(random_array)


# Create a 3 by 3 array with random integers in [10, 20]. Your answer may be different because it is random but it should look something like this:
[[19 11 13]
 [10 11 13]
 [11 14 10]]

random_array = np.random.randint(10, 21, size=(3, 3))

print(random_array)


# Use this array for the following practice:
myArray = np.array([[11,12,13], [14,15,16], [17,18,19]])

# a. Get a subarray of the first row and first 2 columns. Your results should look like this:
[11 12]
 
# b. Change all elements in 1st and second row to 0. Your results should look like this:
[[ 0  0  0]
 [ 0  0  0]
 [17 18 19]]

myArray = np.array([[11,12,13], [14,15,16], [17,18,19]])

subarray_a = myArray[:1, :2]
print("Subarray of the first row and first 2 columns:")
print(subarray_a)

myArray[:2, :] = 0
print("\nArray after changing elements in 1st and second row to 0:")
print(myArray)


# Create an array that contains [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20] and reverse the order.

my_array = np.arange(21)
reverseArray = np.flip(my_array)
print(reverseArray)

# Use this array for the following practice: 
myArray = np.array([[11,12,13], [14,15,16]])

Reshape the array to an array with 3 rows. Your results should look like this:
[[11 12]
 [13 14]
 [15 16]]

myArray = np.array([[11,12,13], [14,15,16]])

reshaped_array = myArray.reshape(3, -1)

print(reshaped_array)


# Use this array for the following practice: 
myArray = np.arange(10)

1. Find the square of every number in array
2. Find the square root of every number in array
3. Multiply the square of each number in array with its respective square root

my_array = np.arange(10)

square_array = np.square(my_array)
print("Squared array is: ", square_array )
sqrt_array = np.sqrt(my_array)
print("\nSquare Root array is: ", sqrt_array)
final_array = square_array * sqrt_array
print("\nSquared Array * Square Root Array is: ", final_array)

# Use this array for the following practice: 
myArray = np.array([[11,12,13], [14,15,16], [17,18,19]])


1. Add a new row of elements containing 20, 21 and 22

2. Add a new column of elements containing 30, 40 and 50

myArray = np.array([[11,12,13], [14,15,16], [17,18,19]])

new_row = np.array([[20, 21, 22]])
myArray = np.concatenate((myArray, new_row), axis=0)

print("Array after adding a new row:")
print(myArray)

new_column = np.array([[30], [40], [50], [0]])  # Ensure the new column has the same number of rows as the original array
myArray = np.concatenate((myArray, new_column), axis=1)

print("\nArray after adding a new column:")
print(myArray)


# INSERTING ELEMENTS 

1. Add 1 column of 1 to this array: myArray = np.zeros((2,2))
2. Add 2 rows of 2 to the answer from part 1
3. Remove the last column
4. Remove the last row



myArray = np.zeros((2, 2))
myArray = np.hstack((myArray, np.ones((2, 1))))

print("Array after adding 1 column of 1:")
print(myArray)

myArray = np.vstack((myArray, np.zeros((2, 3))))
print("\nArray after adding 2 rows of 2:")
print(myArray)

myArray = myArray[:, :-1]
print("\nArray after removing the last column:")
print(myArray)


myArray = myArray[:-1, :]
print("\nArray after removing the last row:")
print(myArray)


# DELETING ELEMENTS


Remove the elements from the middle column of this array:
myArray = np.matrix([[1, 2, 3], [4, 5, 6], [9, 8, 7]])

Your codes should look like this:
[[1 3]
 [4 6]
 [9 7]]

myArray = np.matrix([[1, 2, 3], [4, 5, 6], [9, 8, 7]])

myArray = np.delete(myArray, 1, axis=1)

print("Array after removing the middle column:")
print(myArray)


# Replace all odd numbers in the given array with -1

Start with:
exercise_1 = np.array([0, 1, 2, 3, 4, 5, 6, 7, 8, 9])

Desired output:
[ 0, -1, 2, -1, 4, -1, 6, -1, 8, -1]

exercise_1 = np.array([0, 1, 2, 3, 4, 5, 6, 7, 8, 9])

mask = exercise_1 % 2 != 0

exercise_1[mask] = -1

print(exercise_1)


# Convert a 1-D array into a 2-D array with 3 rows

Start with:
exercise_2 = np.array([0, 1, 2, 3, 4, 5, 6, 7, 8])

Desired output:
[[ 0, 1, 2]
[3, 4, 5]
[6, 7, 8]]

exercise_2 = np.array([0, 1, 2, 3, 4, 5, 6, 7, 8])

result = exercise_2.reshape(3, -1)

print(result)


# Add 202 to all the values in given array

Start with:
exercise_3 = np.arange(4).reshape(2,-1)

Desired output:
[[202, 203]
[204, 205]]

exercise_3 = np.arange(4).reshape(2,-1)

result = exercise_3 + 202
print(result)

# Generate a 1-D array of 10 random integers. Each integer should be a number between 30 and 40 (inclusive)

Sample of desired output: 
[36, 30, 36, 38, 31, 35, 36, 30, 32, 34]

random_array = np.random.randint(30, 41, size=10)

print(random_array)


# Find the positions of:
elements in x where its value is more than its corresponding element in y, and 
elements in x where its value is equals to its corresponding element in y.

Start with these:
x = np.array([21, 64, 86, 22, 74, 55, 81, 79, 90, 89]) 
y = np.array([21, 7, 3, 45, 10, 29, 55, 4, 37, 18])

Desired output:
(array([1, 2, 4, 5, 6, 7, 8, 9]),) and (array([0]),)

x = np.array([21, 64, 86, 22, 74, 55, 81, 79, 90, 89])
y = np.array([21, 7, 3, 45, 10, 29, 55, 4, 37, 18])

more_than_positions = np.where(x > y)

equal_positions = np.where(x == y)

print("Positions where x > y:", more_than_positions)
print("Positions where x == y:", equal_positions)


# Extract the first four columns of this 2-D array
Start with this: 
exercise_6 = np.arange(100).reshape(5,-1)
 
Desired output:
[[ 0 1 2 3]
[20 21 22 23]
[40 41 42 43]
[60 61 62 63]
[80 81 82 83]]

exercise_6 = np.arange(100).reshape(5, -1)

result = exercise_6[:, :4]

print(result)
