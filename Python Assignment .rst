1) What are the types of Applications? 

-->
(i)Web Application : It is software accessed through a web browser that allows users to interact with content or services online.
    For example : Gmail , Google Docs , Amazon
(ii)Business Intelligence(BI) Tools : Help users to create visual data representations and interactive dashboards.
    For example : Tableau , Power BI
(iii)Machine Learning : Support the development of ML models.
    For example : TensorFlow , PyTorch and Scikit-Learn
(iv)Deep Learning Applications : To use neural networks to perform complex tasks like recognizing images and understanding speech.
    For example : TensorFlow , Keras and Caffe

2) What is programing? 

-->Programming is the process of writing instructions for computers to perform specific tasks. It involves using programming languages like Python, Java, or C++ to create algorithms, follow syntax rules, and debug code.

3) What is Python? 

-->Python is a popular programming language. It was created by Guido van Rossum, and released in 1991.
    It is used for:web development , software development , mathematics , system scripting.

.. code:: ipython3

    #4) Write a Python program to check if a number is positive, negative or zero.
    
    # input from the user
    number = float(input("Enter a number: "))
    # Check if the number is positive, negative, or zero
    if number > 0:
        print("This Is A Positive Number")
    elif number < 0:
        print("This Is A Negative Number")
    else:
        print("Zero")


.. parsed-literal::

    Enter a number:  -2.5
    

.. parsed-literal::

    This Is A Negative Number
    

.. code:: ipython3

    #5) Write a Python program to get the Factorial number of given numbers. 
    
    def factorial(number):
        fact = 1  # Initialize factorial to 1
        if number == 0 or number == 1:
            return fact
        else:
            for i in range(1, number + 1):
                fact *= i
        return fact
    # Input from the user
    number = int(input("Enter a number: "))
    result = factorial(number)
    print("The factorial of", number, "is", result)


.. parsed-literal::

    Enter a number:  5
    

.. parsed-literal::

    The factorial of 5 is 120
    

.. code:: ipython3

    #6) Write a Python program to get the Fibonacci series of given range.
    # Input from the user
    num = int(input("Enter the number of terms in the Fibonacci Series: "))
    a, b = 0, 1  # Initialize the first two terms of the Fibonacci series
    # Generate the Fibonacci series
    print("Fibonacci Series:", a, b, end=" ")
    
    for i in range(1, num - 1):
        c = a + b  
        a = b      
        b = c      
        print(c, end=" ") 
    
    print() 


.. parsed-literal::

    Enter the number of terms in the Fibonacci Series:  5
    

.. parsed-literal::

    Fibonacci Series: 0 1 1 2 3 
    

7) How memory is managed in Python?

-->Memory management in Python involves dynamic allocation of memory for objects, utilizing reference counting to track how many references exist for each object. When an object's reference count drops to zero, it is automatically deallocated. Python also employs a garbage collector to clean up circular references that reference counting alone cannot handle.
(i)Dynamic Memory Allocation: Memory is allocated dynamically from the heap when objects are created.
(ii)Reference Counting: Each object maintains a count of references; memory is deallocated when the count reaches zero.
(iii)Memory Pools: Small objects are allocated from memory pools to optimize performance and reduce fragmentation.

8) What is the purpose continuing statement in python? 

-->The continue statement in Python is used within loops to skip the current iteration and move directly to the next one. When continue is encountered, the remaining code inside the loop for that specific iteration is ignored, and the loop proceeds to the next iteration. This is useful when you want to skip specific conditions in a loop without exiting the loop entirely.

.. code:: ipython3

    #9) Write python program that swap two number with temp variable and without temp variable. 
    #Using temp variable
    # Input from the user
    a = int(input("Enter the first number :"))
    b = int(input("Enter the second number :"))
    
    temp = a
    a = b
    b = temp
    # Swapping and displaying results
    print("After swapping :")
    print("a =", a)
    print("b =", b)
    
    #Without using temp variable
    # Input from the user
    a = int(input("Enter the first number :"))
    b = int(input("Enter the second number :"))
    
    a, b = b, a
    # Swapping and displaying results
    print("After swapping (without temp variable):")
    print("a =", a)
    print("b =", b)


.. parsed-literal::

    Enter the first number : 2
    Enter the second number : 5
    

.. parsed-literal::

    After swapping :
    a = 5
    b = 2
    

.. parsed-literal::

    Enter the first number : 10
    Enter the second number : 20
    

.. parsed-literal::

    After swapping (without temp variable):
    a = 20
    b = 10
    

.. code:: ipython3

    #10) Write a Python program to find whether a given number is even or odd, 
    #print out an appropriate message to the user. 
    # Input from the user
    number = int(input("Please enter a number to check if it is even, odd, or zero: "))
    # To check if a number is even or odd
    if number == 0:
        print("Zero is an even number.")
    elif number % 2 == 0:
        print(f"The number {number} is an even number.")
    else:
        print(f"The number {number} is an odd number.")


.. parsed-literal::

    Please enter a number to check if it is even, odd, or zero:  9
    

.. parsed-literal::

    The number 9 is an odd number.
    

.. code:: ipython3

    #11) Write a Python program to test whether a passed letter is a vowel or not.
    # Input from the user
    letter = input("Please enter a letter to check if it is a vowel :")
    # Check if the letter is a vowel
    if letter.lower() in 'aeiou':
        print(f"The letter '{letter}' is a vowel.")
    else:
        print(f"The letter '{letter}' is not a vowel.")


.. parsed-literal::

    Please enter a letter to check if it is a vowel : A
    

.. parsed-literal::

    The letter 'A' is a vowel.
    

.. code:: ipython3

    #12) Write a Python program to sum of three given integers. However, 
    #if two values are equal sum will be zero.
    # Input from the user
    a = int(input("Enter the first integer :"))
    b = int(input("Enter the second integer :"))
    c = int(input("Enter the third integer :"))
    # Check if any two values are equal
    if a == b or b == c or a == c:
        total = 0
    else:
        total = a + b + c
    # Print the result
    print("The sum is :", total)


.. parsed-literal::

    Enter the first integer : 4
    Enter the second integer : 2
    Enter the third integer : 4
    

.. parsed-literal::

    The sum is : 0
    

.. code:: ipython3

    #13) Write a Python program that will return true , 
    #if the two given integer values are equal or their sum or difference is 5. 
    # Input from the user
    a = int(input("Enter the first integer :"))
    b = int(input("Enter the second integer :"))
    
    # Check conditions
    if a == b or abs(a + b) == 5 or abs(a - b) == 5:
        result = True
    else:
        result = False
    
    # Print the result
    print("Result :", result)


.. parsed-literal::

    Enter the first integer : -7
    Enter the second integer : 2
    

.. parsed-literal::

    Result : True
    

.. code:: ipython3

    #14) Write a python program to sum of the first n positive integers. 
    
    # Input from the user
    n = int(input("Enter a positive integer :"))
    
    # Calculate the sum of the first n positive integers
    if n > 0:
        total = 0 
        for i in range(1, n + 1):  
            total += i  
        print(f"The sum of the first {n} positive integers is: {total}")
    else:
        print("Please enter a positive integer.")


.. parsed-literal::

    Enter a positive integer : 3
    

.. parsed-literal::

    The sum of the first 3 positive integers is: 6
    

.. code:: ipython3

    #15) Write a Python program to calculate the length of a string. 
    
    # Input from the user
    string = input("Please enter a string :")
    
    # Calculate the length of the string
    length = len(string)
    
    # Print the result
    print(f"The length of the entered string is : {length}")


.. parsed-literal::

    Please enter a string : Python
    

.. parsed-literal::

    The length of the entered string is : 6
    

.. code:: ipython3

    #16) Write a Python program to count the number of characters(character frequency) in a string.
    
    # Input from the user
    string = input("Please enter a string :")
    frequency = {}  # Initialize a dictionary to hold character frequencies
    
    for char in string:
        if char in frequency:
            frequency[char] += 1  # Increment count if char already exists
        else:
            frequency[char] = 1   # Initialize count for new char
    
    # Print the character frequency
    print("Character frequency in the string:")
    for char in frequency:
        print(f"'{char}': {frequency[char]}")


.. parsed-literal::

    Please enter a string : language
    

.. parsed-literal::

    Character frequency in the string:
    'l': 1
    'a': 2
    'n': 1
    'g': 2
    'u': 1
    'e': 1
    

17) What are negative indexes and why are they used? 

-->Negative indexes in Python are a way to access elements from the end of a sequence, like a list, tuple, or string. Instead of starting from the beginning, negative indexes count backward : -1 accesses the last element, -2 the second-to-last, and so on. This allows for an easy and flexible way to retrieve items from the end without needing to know the length of the sequence.We use negative indexes in Python for convenience and simplicity when accessing elements from the end of a sequence, like a list or string. Negative indexes make it easy to get the last items without needing to calculate the length, helping keep code cleaner and more readable

.. code:: ipython3

    #18) Write a Python program to count occurrences of a substring in a string. 
    
    # Input string and substring from the user
    string = input("Enter the main string :")
    substring = input("Enter the substring to count :")
    
    # Count occurrences of the substring in the main string
    count = string.count(substring)
    
    # Display the result
    print(f"The substring '{substring}' appears {count} times in the main string.")


.. parsed-literal::

    Enter the main string : Python makes coding fun, and coding is a valuable skill.
    Enter the substring to count : coding
    

.. parsed-literal::

    The substring 'coding' appears 2 times in the main string.
    

.. code:: ipython3

    #19) Write a Python program to count the occurrences of each word in a given sentence
    
    # Input from the user
    sentence = input("Enter a sentence: ")
    words = sentence.split()  # Split the sentence into words
    word = {}  # Dictionary to store word counts
    
    # Count occurrences of each word
    for x in words:
        if x in word:
            word[x] += 1
        else:
            word[x] = 1
    
    # Print word counts
    for x, count in word.items():
        print(f"'{x}': {count}")


.. parsed-literal::

    Enter a sentence:  many many returns of the day!
    

.. parsed-literal::

    'many': 2
    'returns': 1
    'of': 1
    'the': 1
    'day!': 1
    

.. code:: ipython3

    #20) Write a Python program to get a single string from two given strings,
    #separated by a space and swap the first two characters of each string.
    
    # Get two strings from the user
    str1 = input("Enter the first string : ")
    str2 = input("Enter the second string : ")
    
    # Swap the first two characters of each string
    if len(str1) < 2 or len(str2) < 2:
        print("Both strings should have at least two characters.")
    else:
         a = str2[:2] + str1[2:]   # Swap first two characters of string1 with string2
         b = str1[:2] + str2[2:]   # Swap first two characters of string2 with string1
    
    # Combine the two strings separated by a space
    combined = a + " " + b
    
    # Output the result
    print("Combined string :", combined)


.. parsed-literal::

    Enter the first string :  happy 
    Enter the second string :  birthday
    

.. parsed-literal::

    Combined string : bippy  harthday
    

.. code:: ipython3

    """21) Write a Python program to add 'in' at the end of a given string (length
    should be at least 3). If the given string already ends with 'ing' then
    add 'ly' instead if the string length of the given string is less than 3,
    leave it unchanged."""
    
    # Get string from the user
    str = input("Enter a string : ")
    
    # Check the length of the string
    if len(str) < 3:
        result = str # If the length is less than 3, leave it unchanged
    else:
        if str.endswith('ing'): # Check if the string ends with 'ing'
            result = str + 'ly'
        else:
            result = str + 'in'  # If it ends with 'ing', add 'ly' instead
    
    # Output the resulting string
    print("Modified string:", result)


.. parsed-literal::

    Enter a string :  Playing
    

.. parsed-literal::

    Modified string: Playingly
    

.. code:: ipython3

    #22) Write a Python function to reverses a string if its length is a multiple of 4. 
    
    def reverse(string):
    
        # Check if the length of the string is a multiple of 4
        if len(string) % 4 == 0:
            return string[::-1]  # Return the reversed string
        else:
            return string   # Return the original string
    
    # Example usage
    str = input("Enter a string : ")
    result = reverse(str)
    print("Result:", result)


.. parsed-literal::

    Enter a string :  Language
    

.. parsed-literal::

    Result: egaugnaL
    

.. code:: ipython3

    #23) Write a Python program to get a string made of the first 2 and the last 2 chars from a given a string.
    #If the string length is less than 2, return instead of the empty string.
    
    def chars(string):
    
        # Check if the length of the string is less than 2
        if len(string) < 2:
            return ""  
        else:
            return string[:2] + string[-2:]  # Return a new string made up of the first two and last two characters
    
    # Example usage
    str = input("Enter a string : ")
    result = chars(str)
    print("Result : ", result)


.. parsed-literal::

    Enter a string :  Python
    

.. parsed-literal::

    Result :  Pyon
    

.. code:: ipython3

    #24) Write a Python function to insert a string in the middle of a string.
    
    def middle(original,insert):
    
        # Find the middle index of the original string
        middle_index = len(original) // 2
    
        # Insert the new string at the middle index
        string = original[:middle_index] + insert + original[middle_index:]
        
        return string
    
    # Example usage
    org_str = input("Enter the original string : ")
    str = input("Enter the string to insert : ")
    result = middle(org_str , str)
    print("Resulting string :", result)


.. parsed-literal::

    Enter the original string :  have a good day!
    Enter the string to insert :  very
    

.. parsed-literal::

    Resulting string : have a gveryood day!
    

25) What is List? How will you reverse a list?

-->Lists are used to store multiple items in a single variable.Lists are one of 4 built-in data types in Python used to store collections of data , all with different qualities and usage.Lists are created using square brackets, e.g., [1, 2, 3], and elements are separated by commas. Lists are mutable, meaning you can modify them by adding, removing, or updating elements. List items are ordered, changeable, and allow duplicate values.
-->To reverse a list, you can use the reverse() method, which directly reverses the list in place, or use slicing [::-1] to create a reversed copy of the list without modifying the original. Another approach is to use the reversed() function, which returns an iterator over the reversed list. Each method is useful depending on whether you need an in-place reversal or a new reversed list.

26) How will you remove last object from a list?

-->To remove the last object from a list in Python, you can use the pop() method without arguments, which removes and returns the last item. 
For example, if you have my_list = [1, 2, 3, 4] and call my_list.pop(), the list becomes [1, 2, 3], and 4 is returned. Another way is to use del my_list[-1], which deletes the last element without returning it. Both methods are efficient and commonly used, with pop() offering the flexibility to retrieve the removed element if needed.

27)Suppose list1 is [2, 33, 222, 14, and 25], what is list1 [-1]? 

-->If list1 is [2, 33, 222, 14, 25], then list1[-1] accesses the last element in the list. In Python, negative indexing starts from the end of the list, with -1 representing the last item. So, list1[-1] would give the value 25. This is because Python allows accessing list elements from the end by using negative indices, which is useful when you want to retrieve items without knowing the exact length of the list.

28) Differentiate between append () and extend () methods?

-->The append() and extend() methods both add elements to a list, but they work differently. 
(i)append() adds its argument as a single element at the end of the list, even if it's another list, creating a nested list if needed. For example, my_list.append([1, 2]) would add [1, 2] as a single item.(ii)extend() iterates over its argument and adds each element individually to the list. So, my_list.extend([1, 2]) would add 1 and 2 as separate elements. Essentially, append() adds one item, while extend() merges multiple items from an iterable.

.. code:: ipython3

    #29) Write a Python function to get the largest number, smallest num 
    #and sum of all from a list. 
    
    def listt(numbers):
        largest = max(numbers)
        smallest = min(numbers)
        total_sum = sum(numbers)
        return largest, smallest, total_sum
    
    # Example usage
    lst = [10, 20, 5, 75, 50]
    largest, smallest, total_sum = listt(lst)
    
    print("Largest number:", largest)
    print("Smallest number:", smallest)
    print("Sum of all numbers:", total_sum)


.. parsed-literal::

    Largest number: 75
    Smallest number: 5
    Sum of all numbers: 160
    

30) How will you compare two lists? 

-->To compare two lists in Python, you can use the == operator for a direct equality check, which verifies that both lists contain the same elements in the same order. If order doesn't matter, you can sort both lists and compare them using sorted(). For checking if one list is a subset of another, you can use the all() function with the in keyword. 
Additionally, if you need to compare lists element-wise, you can loop through both lists using zip() to evaluate each pair of elements. These methods allow you to effectively compare lists based on your specific needs.

.. code:: ipython3

    #31) Write a Python program to count the number of strings where the string length is 2 or more and 
    #the first and last character are same from a given list of strings. 
    
    def count_str(str):
        count = 0
        for string in str:
            if len(string) >= 2 and string[0] == string[-1]:
                count += 1
        return count
    
    # Example usage:
    str = ["abc", "xyz", "aba", "1221", "abcd"]
    result = count_str(str)
    print("Number of matching strings:", result)


.. parsed-literal::

    Number of matching strings: 2
    

.. code:: ipython3

    #32) Write a Python program to remove duplicates from a list.
    
    def duplicates(lst):
        return list(dict.fromkeys(lst))
    
    # Example usage:
    lst = [1, 2, 3, 2, 4, 1, 5]
    listt = duplicates(lst)
    print("List after removing duplicates :", listt)


.. parsed-literal::

    List after removing duplicates : [1, 2, 3, 4, 5]
    

.. code:: ipython3

    #33) Write a Python program to check a list is empty or not.
    
    def empty(lstt):
        return len(lstt) == 0
    
    # Example usage:
    listt = []
    if empty(listt):
        print("The list is empty.")
    else:
        print("The list is not empty.")


.. parsed-literal::

    The list is empty.
    

.. code:: ipython3

    #34) Write a Python function that takes two lists and returns true if they have at least one common member. 
    
    def common(list1, list2):
    
        # Iterate through each element in the first list
        for x in list1:
            # Check if the current item is in the second list
            if x in list2:
                return True
        return False
    
    # Example usage:
    a = [1, 2, 3, 4]
    b = [5, 6, 3, 7]
    
    if common(a,b):
        print("The lists have at least one common member.")
    else:
        print("The lists do not have any common members.")


.. parsed-literal::

    The lists have at least one common member.
    

.. code:: ipython3

    #35) Write a Python program to generate and print a list of first and last 5 elements 
    #where the values are square of numbers between 1 and 30. 
    
    def elements():
        
        squares = []  # Initialize an empty list to hold the squares
    
        # Use a for loop to generate squares for numbers between 1 and 30
        for i in range(1, 31):
            squares.append(i**2)   # Append the square of the current number to the list
    
        # Get the first 5 elements
        first_five = squares[:5]
         # Get the last 5 elements
        last_five = squares[-5:]
        
        return first_five, last_five
    
    # Example usage
    first_five, last_five = elements()
    print("First 5 squares:", first_five)
    print("Last 5 squares:", last_five)


.. parsed-literal::

    First 5 squares: [1, 4, 9, 16, 25]
    Last 5 squares: [676, 729, 784, 841, 900]
    

.. code:: ipython3

    #36) Write a Python function that takes a list and returns a new list with unique elements of the first list. 
    
    def elements(input_list):
        newlist = []    # Initialize an empty list to store unique elements
        
        for i in input_list:
            if i not in newlist:  # Check if the item is not already in the unique list
                newlist.append(i)  # Add it to the unique list if it's not present
        
        return newlist
    
    # Example usage:
    lst = [1, 2, 2, 3, 4, 1, 5]
    result = elements(lst)
    print("Unique elements:", result)


.. parsed-literal::

    Unique elements: [1, 2, 3, 4, 5]
    

.. code:: ipython3

    #37) Write a Python program to convert a list of characters into a string.
    
    def str(char):
        # Join the list of characters into a single string
        return ''.join(char)
    
    # Example usage:
    char = ["H", "o", "w", " " , "a", "r", "e", " ", "y", "o", "u", "?"]
    result = str(char)
    print("Converted string :", result)


.. parsed-literal::

    Converted string : How are you?
    

.. code:: ipython3

    #38) Write a Python program to select an item randomly from a list.
    
    import random
    
    def randomm(lst):
        # Use random.choice() to select a random item from the list
        return random.choice(lst)
    
    # Example usage:
    my_list = ["hello" , "world" , "good" , 12 , True]
    random_item = randomm(my_list)
    print("Randomly selected item:", random_item)


.. parsed-literal::

    Randomly selected item: good
    

.. code:: ipython3

    #39) Write a Python program to find the second smallest number in a list.
    
    def smallest(numbers):
        # Remove duplicates by converting the list to a set and back to a list
        unique_numbers = list(set(numbers))
    
        # Check if there are at least two unique numbers
        if len(unique_numbers) < 2:
            return None  
        
       # Sort the list
        unique_numbers.sort()
       # Return the second smallest number
        return unique_numbers[1]
    
    # Example usage:
    my_list = [3, 5, 1, 4, 2, 1]
    result = smallest(my_list)
    
    if result is not None:
        print("The second smallest number is:", result)
    else:
        print("There is no second smallest number in the list.")


.. parsed-literal::

    The second smallest number is: 2
    

.. code:: ipython3

    #40) Write a Python program to get unique values from a list.
    
    def values(lstt):
        valuee = list(set(lstt)) # Convert to set to remove duplicates, then back to list 
        return valuee
    
    # Example usage:
    my_list = [1, 2, 2, 3, 4, 4, 5, 6, 6, 7]
    newlist = values(my_list)
    print("Unique values:", newlist)


.. parsed-literal::

    Unique values: [1, 2, 3, 4, 5, 6, 7]
    

.. code:: ipython3

    #41) Write a Python program to check whether a list contains a sub list.
    
    def contain(mainlist, sublist):
       # Get the length of the main list and sublist
        mainlen = len(mainlist)
        sublen = len(sublist)
    
         # Check if sublist is longer than the main list
        if sublen > mainlen:
            return False
    
        # Iterate through the main list to check for sublist
        for i in range(mainlen - sublen + 1):
            # Check if the current segment matches the sublist
            if mainlist[i:i + sublen] == sublist:
                return True  # Sublist found 
    
        return False  # Sublist not found
    
    # Example usage:
    mainlist = [1, 2, 3, 4, 5, 6]
    sublist = [3, 4, 5]
    result = contain(mainlist, sublist)
    
    if result:
        print("The list contains the sublist.")
    else:
        print("The list does not contain the sublist.")


.. parsed-literal::

    The list contains the sublist.
    

.. code:: ipython3

    #42) Write a Python program to split a list into different variables. 
    
    # Original list
    lst = [1, 2, 3, 4]
    
    # Unpack the list into variables
    a, b, c, d = lst
    
    # Display each variable
    print("a:", a)
    print("b:", b)
    print("c:", c)
    print("d:", d)


.. parsed-literal::

    a: 1
    b: 2
    c: 3
    d: 4
    

43) What is tuple? Difference between list and tuple. 

-->Tuples are used to store multiple items in a single variable,tuple is one of 4 built-in data types in Python used to store collections of data
A tuple is a collection which is ordered and unchangeable.Tuples are written with round brackets.Tuple items allow duplicate values.Tuple items are indexed, the first item has index [0], the second item has index [1] etc.
Lists are mutable and have more built-in methods for adding, removing, or changing elements. Because tuples are fixed and unchangeable, they are generally faster and are used when a constant, unchangeable sequence is needed.

.. code:: ipython3

    #44) Write a Python program to create a tuple with different data types. 
    
    # Creating a tuple with different data types
    tup= (1, "Hello", 3.14, True, None)
    
    # Displaying the tuple
    print("Tuple with different data types:", tup)
    
    # Accessing elements in the tuple
    print("First element:", tup[0])       
    print("Second element:", tup[1])      
    print("Third element:", tup[2])       
    print("Fourth element:", tup[3])      
    print("Fifth element:", tup[4])       


.. parsed-literal::

    Tuple with different data types: (1, 'Hello', 3.14, True, None)
    First element: 1
    Second element: Hello
    Third element: 3.14
    Fourth element: True
    Fifth element: None
    

.. code:: ipython3

    #45) Write a Python program to unzip a list of tuples into individual lists.
    
    # List of tuples
    lst = [(1, 'a'), (2, 'b'), (3, 'c'), (4, 'd')]
    
    # Unzipping into individual lists
    numbers, letters = zip(*lst)
    
    # Converting the result to lists (optional)
    numbers = list(numbers)
    letters = list(letters)
    
    # Displaying the results
    print("List of numbers:", numbers)
    print("List of letters:", letters)


.. parsed-literal::

    List of numbers: [1, 2, 3, 4]
    List of letters: ['a', 'b', 'c', 'd']
    

.. code:: ipython3

    #46) Write a Python program to convert a list of tuples into a dictionary. 
    
    # List of tuples
    listt = [(1, 'apple'), (2, True), (3, 'cherry')]
    
    # Converting to dictionary
    dictt = dict(listt)
    
    # Displaying the result
    print("Dictionary:", dictt)


.. parsed-literal::

    Dictionary: {1: 'apple', 2: True, 3: 'cherry'}
    

#47) How will you create a dictionary using tuples in python?

-->In Python, you can create a dictionary from tuples by using the dict() function. Each tuple should contain exactly two elements: the first element becomes the key, and the second element becomes the value in the dictionary. This method works well with a list of tuples or even a tuple of tuples, where each two-item tuple represents a key-value pair. By converting the list or tuple of tuples directly to a dictionary, you can quickly set up key-value mappings. This approach is useful when you have structured data that you want to convert into a dictionary format for easier lookup.

.. code:: ipython3

    #48) Write a Python script to sort (ascending and descending) a dictionary by value. 
    
    # Sample dictionary
    dictt = {'apple': 10, 'banana': 5, 'cherry': 20, 'date': 15}
    
    # Define a function to return the value of a dictionary item
    def value(item):
        return item[1]
    
    # Sorting in ascending order by value
    Sorted = sorted(dictt.items(), key=value)
    ascending = dict(Sorted)
    
    # Sorting in descending order by value
    sorted_ = sorted(dictt.items(), key=value, reverse=True)
    descending = dict(sorted_)
    
    # Displaying the results
    print("Dictionary sorted by value in ascending order:", ascending)
    print("Dictionary sorted by value in descending order:", descending)


.. parsed-literal::

    Dictionary sorted by value in ascending order: {'banana': 5, 'apple': 10, 'date': 15, 'cherry': 20}
    Dictionary sorted by value in descending order: {'cherry': 20, 'date': 15, 'apple': 10, 'banana': 5}
    

.. code:: ipython3

    #49) Write a Python script to concatenate following dictionaries to create a new one.
    
    # Sample dictionaries
    dict1 = {'a': 1, 'b': 2}
    dict2 = {'b': 3, 'c': 4}
    dict3 = {'d': 5}
    
    # Create a new dictionary and update it with dict1 and dict2
    new_dict = dict1.copy()  # Create a copy of dict1 to avoid modifying it
    new_dict.update(dict2)   # Update with dict2
    new_dict.update(dict3)   # Update with dict3
    
    # Display the result
    print("Concatenated dictionary :", new_dict)


.. parsed-literal::

    Concatenated dictionary : {'a': 1, 'b': 3, 'c': 4, 'd': 5}
    

.. code:: ipython3

    #50)Write a Python script to check if a given key already exists in a dictionary. 
    
    # Sample dictionary
    dictt = {
        
        "name": "Alice",
        "age": 25,
        "city": "New York"
    }
    # Function to check if a key exists in the dictionary
    def exists(dictionary, key):
        if key in dictionary:
            return True
        else:
            return False
    
    # Input key to check
    check = input("Enter a key : ")
    
    # Check if the key exists and display the result
    if exists(dictt , check):
        print(f"The key '{check}' exists in the dictionary.")
    else:
        print(f"The key '{check}' does not exist in the dictionary.")


.. parsed-literal::

    Enter a key :  city
    

.. parsed-literal::

    The key 'city' exists in the dictionary.
    

51) How Do You Traverse Through a Dictionary Object in Python? 

-->Traversing through a dictionary in Python involves iterating over its key-value pairs to access or manipulate the data stored within. You can use a for loop to loop directly over the keys, allowing you to retrieve each value using the key. Alternatively, the .items() method enables simultaneous access to both keys and values in the form of tuples. If you only need to work with keys or values, you can utilize the .keys() or .values() methods, respectively. These methods provide a straightforward and efficient way to navigate and interact with dictionary contents in Python.

52)How Do You Check the Presence of a Key in A Dictionary? 

-->To check for the presence of a key in a dictionary in Python, you can use the "in" keyword, which provides a simple and efficient way to verify whether a specified key exists. By using the expression key in dictionary, Python checks if the key is present and returns True if it is, and False otherwise. This approach is straightforward and avoids the need for additional function calls, making it the preferred method for key presence checks. Additionally, the get() method can be used, which returns the value associated with the key if it exists, or a default value if it does not, allowing for a more flexible way to handle key lookups.

.. code:: ipython3

    #53) Write a Python script to print a dictionary where the keys are numbers between 1 and 15. 
    
    # Initialize an empty dictionary for the multiplication table
    newdict = {}
    
    # Populate the dictionary with keys from 1 to 15 and values as 2 times the key
    for i in range(1, 16):
        newdict[i] = i*2     # Assigning 2 multiplied by i as the value for key i
        
    # make a table using key numbers between 1 and 15
    for key, value in newdict.items():
        print(f"2 x {key} = {value}")


.. parsed-literal::

    2 x 1 = 2
    2 x 2 = 4
    2 x 3 = 6
    2 x 4 = 8
    2 x 5 = 10
    2 x 6 = 12
    2 x 7 = 14
    2 x 8 = 16
    2 x 9 = 18
    2 x 10 = 20
    2 x 11 = 22
    2 x 12 = 24
    2 x 13 = 26
    2 x 14 = 28
    2 x 15 = 30
    

.. code:: ipython3

    #54)Write a Python program to check multiple keys exists in a dictionary.
    
    # Sample dictionary
    dictt = {
        'name': 'Alice',
        'age': 25,
        'city': 'New York',
        'profession': 'Engineer'
    }
    
    # List of keys to check
    check = ['name', 'age', 'country', 'city']
    
    # Function to check if multiple keys exist in the dictionary
    def check_keys(dictionary, keys):
        missing_keys = []     # List to store any missing keys
        for key in keys:
            if key not in dictionary:
                missing_keys.append(key)    # Add missing key to the list
        return missing_keys
    
    # Check keys and display the result
    missing_keys = check_keys(dictt,check)
    
    if missing_keys:
        print(f"The following keys do not exist in the dictionary: {', '.join(missing_keys)}")
    else:
        print("All keys exist in the dictionary.")


.. parsed-literal::

    The following keys do not exist in the dictionary: country
    

.. code:: ipython3

    #55) Write a Python script to merge two Python dictionaries.
    
    # Define two dictionaries
    dict1 = {'a': 1, 'b': 2, 'c': 3}
    dict2 = {'b': 4, 'd': 5, 'e': 6}
    
    # Merge dictionaries using the update() method
    merged = dict1.copy()     # Create a copy of the first dictionary
    merged.update(dict2)      # Update with the second dictionary
    
    # Print the merged dictionary
    print("Merged dictionary:", merged)


.. parsed-literal::

    Merged dictionary: {'a': 1, 'b': 4, 'c': 3, 'd': 5, 'e': 6}
    

.. code:: ipython3

    #56) Write a Python program to map two lists into a dictionary.
    #Sample output: Counter ({'a': 400, 'b': 400,’d’: 400, 'c': 300}). 
    
    from collections import Counter
    
    # Sample lists
    keys = ['a', 'b', 'c', 'd']
    values = [400, 400, 300, 400]
    
    # Map the lists into a dictionary using zip, then convert to Counter
    mapped_counter = Counter(dict(zip(keys, values)))
    
    # Print the result in the desired format
    print(mapped_counter, sep="")


.. parsed-literal::

    Counter({'a': 400, 'b': 400, 'd': 400, 'c': 300})
    

.. code:: ipython3

    #57) Write a Python program to find the highest 3 values in a dictionary.
    
    # Sample dictionary
    dictt = {'a': 50, 'b': 200, 'c': 150, 'd': 400, 'e': 300}
    
    # Sort the dictionary items by value in descending order and select the top 3
    top_3 = sorted(dictt.values(), reverse=True)[:3]
    
    print("The highest 3 values are:", top_3)


.. parsed-literal::

    The highest 3 values are: [400, 300, 200]
    

.. code:: ipython3

    #58) Write a Python program to combine values in python list of dictionaries.
    #Sample data: [{'item': 'item1', 'amount': 400}, {'item': 'item2', 'amount':300}, o {'item': 'item1', 'amount': 750}]
    
    # Sample data
    data = [
        {'item': 'item1', 'amount': 400},
        {'item': 'item2', 'amount': 300},
        {'item': 'item1', 'amount': 750}
    ]
    
    # Dictionary to store the combined amounts
    result = {}
    
    # Loop through each dictionary in the list
    for entry in data:
        item = entry['item']
        amount = entry['amount']
    
        # Add amount to the existing total if item already exists, else initialize it
        if item in result:
            result[item] += amount
        else:
            result[item] = amount
    
    # Print the result in a Counter-like format
    print("Counter({", end="")
    pairs = []
    for key, value in result.items():
        pairs.append("'" + str(key) + "': " + str(value))
    
    print(" , ".join(pairs), end="")
    print("})")


.. parsed-literal::

    Counter({'item1': 1150 , 'item2': 300})
    

.. code:: ipython3

    #59)Write a Python program to create a dictionary from a string.
    #Note: Track the count of the letters from the string. 
    
    # Sample string
    string = "good evening"
    
    # Dictionary to hold letter counts
    count = {}
    
    # Loop through each character in the string
    for char in string:
        # Ignore spaces
        if char != " ":
             # Update the count for the character
            if char in count:
                count[char] += 1
            else:
                count[char] = 1
    
    # Print the resulting dictionary
    print(count)


.. parsed-literal::

    {'g': 2, 'o': 2, 'd': 1, 'e': 2, 'v': 1, 'n': 2, 'i': 1}
    

.. code:: ipython3

    #60) Sample string:
    # 'w3resource' Expected output:
    #• {'3': 1,’s’: 1, 'r': 2, 'u': 1, 'w': 1, 'c': 1, 'e': 2, 'o': 1}
    
    # Sample string
    string = 'w3resource'
    # Dictionary to hold letter counts
    count = {}
    
    # Loop through each character in the string
    for char in string:
        # Update the count for the character
        if char in count:
            count[char] += 1
        else:
            count[char] = 1
    
    # Prepare to construct the output string
    pairs = []
    
    # Specify the order of keys
    order = ['3', 's', 'r', 'u', 'w', 'c', 'e', 'o']
    for key in order:
       pairs.append(f"'{key}': {count[key]}")
        
    # Join the pairs into a string and print the result
    print("{" + " , ".join(pairs) + "}")


.. parsed-literal::

    {'3': 1 , 's': 1 , 'r': 2 , 'u': 1 , 'w': 1 , 'c': 1 , 'e': 2 , 'o': 1}
    

.. code:: ipython3

    #61) Write a Python function to calculate the factorial of a number (a nonnegative integer).
    
    def factorial(number):
        fact = 1   # Initialize the fact to 1
        if number < 0:
            return "Factorial is not defined for negative numbers."
        elif number == 0 or number == 1:
            return fact
        else:
            for i in range(1, number + 1):
                fact *= i
        return fact
    
    # Input from the user
    number = int(input("Enter a number: "))
    result = factorial(number)
    print("The factorial of", number, "is", result)


.. parsed-literal::

    Enter a number:  3
    

.. parsed-literal::

    The factorial of 3 is 6
    

.. code:: ipython3

    #62) Write a Python function to check whether a number is in a given range.
    
    def range(number, start, end):
        return start <= number <= end   #Check if the number is in the specified range 
    
    # Input from the user
    num = int(input("Enter a number to check if it's in the range: "))
    start_range = int(input("Enter the start of the range: "))
    end_range = int(input("Enter the end of the range: "))
    
    if range(num, start_range, end_range):
        print(f"{num} is in the range [{start_range}, {end_range}].")
    else:
        print(f"{num} is not in the range [{start_range}, {end_range}].")


.. parsed-literal::

    Enter a number to check if it's in the range:  5
    Enter the start of the range:  1
    Enter the end of the range:  10
    

.. parsed-literal::

    5 is in the range [1, 10].
    

.. code:: ipython3

    #63) Write a Python function to check whether a number is perfect or not.
    
    def is_perfect(number):
        if number < 1:
            return False  # Negative numbers and 0 are not perfect numbers
        
        # Find divisors and sum them
        divisors_sum = 0
        for i in range(1,number):  # Range starts at 1 and goes up to (but not including) 'number'
            if number % i == 0:
                divisors_sum += i
    
        # Check if the sum of divisors equals the number
        return divisors_sum == number
    
    # Test the function
    num = int(input("Enter a number to check if it's perfect: "))
    if is_perfect(num):
        print(f"{num} is a perfect number.")
    else:
        print(f"{num} is not a perfect number.")


.. parsed-literal::

    Enter a number to check if it's perfect:  6
    

.. parsed-literal::

    6 is a perfect number.
    

.. code:: ipython3

    #64) Write a Python function that checks whether a passed string is palindrome or not.
    
    def is_palindrome(s):
    
         # String by removing spaces and converting to lowercase
        str = s.replace(" ", "").lower()
        # Check if the string is equal to its reverse
        return str == str[::-1]
    
    # Example usage
    string = input("Enter a string to check if it's a palindrome: ")
    if is_palindrome(string):
        print(f'"{string}" is a palindrome.')
    else:
        print(f'"{string}" is not a palindrome.')


.. parsed-literal::

    Enter a string to check if it's a palindrome:  Level
    

.. parsed-literal::

    "Level" is a palindrome.
    

65) How Many Basic Types of Functions Are Available in Python?

-->Python has several basic types of functions that help perform different tasks. 
(i)Built-in functions are pre-defined and can be used directly, like print() and len(). 
(ii)User-defined functions are created by users using the def keyword to carry out specific actions. 
(iii)Anonymous functions, or lambda functions, are small, unnamed functions that can be created in one line. 
(iv)Recursive functions call themselves to solve problems, like calculating factorials. 
(v)Higher-order functions can take other functions as arguments or return them, while generator functions use yield to create sequences of values one at a time. 
Each type of function serves a unique purpose in programming.

66)How can you pick a random item from a list or tuple?

-->To pick a random item from a list or tuple in Python, you can use the random.choice() function from the random module. This function takes the list or tuple as an argument and returns a randomly selected item. 
For example, you can do this by first importing the random module and then calling random.choice(your_list) or random.choice(your_tuple) to get a random element from the collection.

67) How can you pick a random item from a range? 

-->To pick a random item from a range in Python, you can use the random.randint() function from the random module. This function allows you to specify the start and end of the range, inclusive. For example, you can get a random integer between 1 and 10 by calling random.randint(1, 10). Alternatively, you can use random.choice() in combination with range(), like random.choice(range(1, 11)), which achieves the same result by converting the range into a list of numbers.

68) How can you get a random number in python? 

-->In Python, you can generate a random number using the random module, which provides several functions. The random.random() function returns a floating-point number between 0.0 and 1.0. To get a random integer within a specific range, you can use random.randint(a, b), which returns a random integer between a and b, inclusive. For random numbers from a range with a specified step, random.randrange(start, stop, step) can be used. If you need a random floating-point number within a specific range, use random.uniform(a, b). Don't forget to import the random module first with import random.

69) How will you set the starting value in generating random numbers? 

-->To set the starting value for generating random numbers in Python, you use the random.seed() function from the random module. Setting a seed ensures that the sequence of random numbers generated is reproducible.
For example, calling random.seed(10) will set the starting point, so every time you run the program with this seed, you’ll get the same sequence of random numbers. This is especially useful for debugging or when you want consistent results in simulations.

.. code:: ipython3

    #70) How will you randomize the items of a list in place?
    
    """To randomize or shuffle the items of a list in place in Python, you can use the random.
    shuffle() function from the random module. This function modifies the list directly,rearranging its elements in a random order.
    Here’s how to use it:"""
    
    import random
    
    lst = [1, 2, 3, 4, 5]
    random.shuffle(lst)
    print(lst)
    
    #Each time you run this code, lst will be shuffled into a different random order. 
    #Note that shuffle() only works with mutable sequences, like lists, and not with tuples or strings.


.. parsed-literal::

    [1, 5, 3, 2, 4]
    

71) What is File function in python? What are keywords to create and write file. 

-->In Python, the file function typically refers to the open() function. file handling is done with the open() function, which opens a file for various operations like reading, writing, or appending. Key modes include
'w' to write (creates or overwrites), 
'a' to append (adds to the end or creates if missing), and 
'x' to exclusively create a file (errors if it exists). 
Closing the file afterward with file.close() ensures changes are saved. 
For example, open("file.txt", "w") will open (or create) "file.txt" for writing, allowing you to write data to it directly.

.. code:: ipython3

    #72) Write a Python program to read an entire text file. 
    
    a = open("file(72).txt", "r")
    content = a.read()  
    print(content)         


.. parsed-literal::

    Hello!!
    Good Morning...
    how are you??
    what are you doing??
    
    

.. code:: ipython3

    #73) Write a Python program to append text to a file and display the text.
    
    append = "have a great day!"
    
    a = open("file(72).txt" , "a")
    b = a.write(append + "\n") 
    
    b = open("file(72).txt" , "r")
    content = b.read()
    print(content)         


.. parsed-literal::

    Hello!!
    Good Morning...
    how are you??
    what are you doing??
    have a great day!
    
    

.. code:: ipython3

    #74) Write a Python program to read first n lines of a file. 
    
    def read(filename, n):
        b = open(filename, "r")  
        for i in range(n):
            line = b.readline()    
            if not line:           
                break
            print(line.strip())   
        b.close()                 
    
    filename = "file(72).txt"  
    n = 3                       
    
    read(filename, n)


.. parsed-literal::

    Hello!!
    Good Morning...
    how are you??
    

.. code:: ipython3

    #75) Write a Python program to read last n lines of a file. 
    
    def read(filename, n):
        b = open(filename, "r")  
        lines = b.readlines()    
        b.close()                 
    
        for line in lines[-n:]:  
            print(line.strip())   
    
    filename = "file(72).txt"  
    n = 3                       
    
    read(filename, n)


.. parsed-literal::

    how are you??
    what are you doing??
    have a great day!
    

.. code:: ipython3

    #76) Write a Python program to read a file line by line and store it into a list.
    
    def read(filename):
        lines = []  
        b = open(filename, "r")  
        for line in b:          
            lines.append(line.strip()) 
        b.close()                
        return lines             
    
    filename = "file(72).txt" 
    
    lst = read(filename)
    print(lst)


.. parsed-literal::

    ['Hello!!', 'Good Morning...', 'how are you??', 'what are you doing??', 'have a great day!']
    

.. code:: ipython3

    #77) Write a Python program to read a file line by line store it into a variable. 
    
    def variable(filename):
        content = ""  
        b = open(filename, "r")  
        for line in b:  
            content += line 
        b.close() 
        return content 
    
    filename = "file(72).txt"  
    
    file = variable(filename)
    print(file)


.. parsed-literal::

    Hello!!
    Good Morning...
    how are you??
    what are you doing??
    have a great day!
    
    

.. code:: ipython3

    #78) Write a python program to find the longest words.
    
    def find_longest_words(word_list):
        # Check if the word list is empty
        if not word_list:
            return []
    
        # Initialize variables to track the longest words and their length
        length = 0
        longest_words = []
    
        # Iterate through the list of words
        for word in word_list:
            # Check the length of the current word
            word_length = len(word)
    
            # Update max_length and reset longest_words if we found a longer word
            if word_length > length:
                length = word_length
                longest_words = [word]  # Start a new list with the new longest word
            elif word_length == length:
                longest_words.append(word)  # Add to the list of longest words
    
        return longest_words
    
    # Example usage
    words = input("Enter a list of words separated by spaces: ").split()
    longest_words = find_longest_words(words)
    print("Longest word:", longest_words)


.. parsed-literal::

    Enter a list of words separated by spaces:  This is a python programming!!
    

.. parsed-literal::

    Longest word: ['programming!!']
    

.. code:: ipython3

    #79) Write a Python program to count the number of lines in a text file. 
    
    # Function to count the number of lines in a file
    def lines(filename):
        count = 0        # Initialize the count
     
        b = open("file(72).txt" , "r")   # Open the file in read mode
        for line in b:
            count += 1      # Increment the line counter for each line
        b.close()           # Close the file
        return count        # Return the total count of lines
    
    # Example usage
    filename = "file(72).txt" 
    total_lines = lines(filename)
    print(f"The number of lines in the file '{filename}' is: {total_lines}")


.. parsed-literal::

    The number of lines in the file 'file(72).txt' is: 5
    

.. code:: ipython3

    #80) Write a Python program to count the frequency of words in a file. 
    
    # Function to count the frequency of words in a file
    def frequency(filename):
        word_frequency = {}      # Initialize a dictionary to store word frequencies
    
        b = open("file(72).txt" , "r")    # Open the file in read mode
        for line in b:
                words = line.lower().split()
                for w in words:
                    if w in word_frequency:
                        word_frequency[w] += 1 
                    else:
                        word_frequency[w] = 1  
    
        return word_frequency
    
    # Usage example
    filename = "file(72).txt" 
    count = frequency(filename)
    
    for w, count in count.items():
        print(f"{w}: {count}")   # Print each word and its frequency


.. parsed-literal::

    hello!!: 1
    good: 1
    morning...: 1
    how: 1
    are: 2
    you??: 1
    what: 1
    you: 1
    doing??: 1
    have: 1
    a: 1
    great: 1
    day!: 1
    

.. code:: ipython3

    #81) Write a Python program to write a list to a file. 
    
    def file(filename,listt):
        a = open(filename, "w")   # Store the file object in a variable
        for item in listt:
            a.write(f"{item}\n")     # Write each item to a new line
    
    # Example usage
    filename = "file(81).txt"
    listt = ["python", "language", 13 , True , 22.3]
    
    file(filename, listt)
    print(f"The list has been written to {filename}.")


.. parsed-literal::

    The list has been written to file(81).txt.
    

.. code:: ipython3

    #82) Write a Python program to copy the contents of a file to another file.
    
    def copy(source, destination):
         # Open the source file in read mode
        src = open(source, "r")  
         # Open the destination file in write mode
        dest = open(destination, "w")  
    
         # Loop through each line in the source file and write it to the destination file
        for line in src:
            dest.write(line)  
    
         # Close both files to save and release resources
        src.close()
        dest.close()
    
    # Example usage
    source = "source.txt"
    destination = "destination.txt"
    
    copy(source , destination)
    print(f"Contents of {source} have been copied to {destination}.")


.. parsed-literal::

    Contents of source.txt have been copied to destination.txt.
    

83) Explain Exception handling? What is an Error in Python? 

-->Exception handling in Python refers to the process of responding to the occurrence of exceptions—unforeseen events or errors that disrupt the normal flow of a program. When an error occurs, Python raises an exception, which can be handled using try, except, else, and finally blocks. This allows programmers to gracefully manage errors, preventing crashes and providing meaningful feedback. An error in Python can occur for various reasons, such as syntax errors, runtime errors (like division by zero), or logical errors (incorrect results due to flawed logic). Effective exception handling improves code robustness by allowing developers to anticipate and manage potential issues without abrupt program termination.

84) How many except statements can a try-except block have? Name Some built-in exception classes:

-->A try-except block in Python can have multiple except statements to handle different types of exceptions that may arise during the execution of the code inside the try block. This allows for more specific error handling depending on the type of exception raised. There is no strict limit on the number of except statements you can have in a single try block, but it's generally advisable to keep it manageable and clear.
-->Some built-in exception classes:
(i)ZeroDivisionError: Raised when attempting to divide a number by zero.
(ii)AttributeError: Raised when an invalid attribute reference is made.
(iii)NameError: Raised when trying to access a variable that has not been defined.
(iv)IndexError: Raised when trying to access an index that is out of range for a list or a tuple.
(v)KeyError: Raised when trying to access a dictionary with a key that does not exist.
etc...

85) When will the else part of try-except-else be executed?

-->The else part of a try-except-else block in Python is executed only when the code within the try block does not raise any exceptions. This means that if the try block runs successfully without encountering an error, the code inside the else block will execute next. It is commonly used to define code that should run only if the try block succeeds, allowing for a clear separation between error handling and normal execution flow. If an exception occurs, the else block is skipped entirely.

86) Can one block of except statements handle multiple exception? 

-->Yes, one block of except statements can handle multiple exceptions in Python. This is done by specifying a tuple of exception types in a single except clause. When an exception is raised in the try block, Python checks the type of the exception and matches it against the specified types in the tuple. If there is a match, the code inside that except block will execute, allowing you to handle various exceptions with the same logic. This approach simplifies the code and keeps it clean by reducing redundancy, as you can define a single error-handling routine for multiple potential errors, rather than having separate except blocks for each exception type.

87) When is the finally block executed? 

-->The finally block in Python is executed after the try and except blocks have completed, regardless of whether an exception was raised or not. This means that the code within the finally block will run after the try block finishes executing, and it will also run if an exception occurs and is caught in the except block. The primary purpose of the finally block is to ensure that certain cleanup actions, such as closing files or releasing resources, are always performed, regardless of whether the code executed successfully or encountered an error. Even if the program encounters a return statement or an unhandled exception within the try or except blocks, the code in the finally block will still execute.

88) What happens when „1‟== 1 is executed? 

-->When the expression „1‟ == 1 is executed in Python, it evaluates to False. This is because the left operand is a string („1‟) and the right operand is an integer (1). Python performs a type comparison when evaluating equality. Since the types of the two operands are different (string vs. integer), Python determines that they are not equal, resulting in the output False. In summary, the expression checks for equality and, due to the type mismatch, the comparison fails, returning False.

89) How Do You Handle Exceptions with Try/Except/Finally in Python? 

-->In Python, exceptions are handled using the try, except, and finally blocks. The try block contains code that may raise an exception, while the except block catches and handles specific exceptions, allowing the program to continue running without crashing. The finally block executes regardless of whether an exception occurred, making it ideal for cleanup tasks, such as closing files or releasing resources. This structured approach enables developers to manage errors effectively, ensuring robust and error-resistant code.

.. code:: ipython3

    #89) Explain with coding snippets.
    
    def divide(num1, num2):
        try:
            result = num1 / num2    # Attempt to divide the numbers
            print(f"The result of division is: {result}")
        except ZeroDivisionError:
            print("Error: Cannot divide by zero.")      # Handle division by zero without capturing the exception
        except TypeError:
            print("Error: Invalid input type.")        # Handle incorrect input types
        finally:  
            print("Execution complete.")              # This block always executes
    
    # Test the function with different inputs
    divide(10, 2)      # Valid division 
    divide(10, 0)      # Division by zero
    divide(10, 'a')    # Invalid type


.. parsed-literal::

    The result of division is: 5.0
    Execution complete.
    Error: Cannot divide by zero.
    Execution complete.
    Error: Invalid input type.
    Execution complete.
    

.. code:: ipython3

    #90)Write python program that user to enter only odd numbers,else will raise an exception. 
    
    def odd():
        while True:      # Loop until a valid odd number is entered
            try:
                user = int(input("Please enter an odd number: "))    # Prompt user for input
                
                if user % 2 == 0:     # Check if the number is even
                    raise ValueError("The number entered is even. Please enter an odd number.")  
    
                print(f"You have entered the odd number: {user}")     # Success message
                break     # Exit the loop if a valid odd number is entered
    
            except ValueError as e:    # Handle ValueError
                print(e)    # Print the error message
    
    # Call the function
    odd()


.. parsed-literal::

    Please enter an odd number:  2
    

.. parsed-literal::

    The number entered is even. Please enter an odd number.
    

.. parsed-literal::

    Please enter an odd number:  5
    

.. parsed-literal::

    You have entered the odd number: 5
    

