# Learn Python for Data Analyst Part 2

Welcome back to the continuation of our Python Mastery for Data Analysts guide! 🐍

In Part 2, we'll delve even deeper into the world of Python programming, building upon the foundational knowledge you gained in Part 1. This section will cover more advanced topics that are crucial for data analysis, including functions, NumPy, Pandas (Series & DataFrame), datetime, Random Library, and txt file - open, read, close.

By exploring these concepts, you'll further enhance your Python skills and be well-prepared to tackle real-world data analysis tasks. Each topic is accompanied by a brief explanation to help you understand its purpose and relevance in Python programming.

## Function

A function is a block of code that performs a specific task. It allows you to organize your code into reusable components, making it easier to manage and maintain. Functions can take input parameters, perform operations, and return output values.

- **Definition**:

  - Define a function using the `def` keyword followed by the function name and parentheses containing any input parameters.

    <div align="center"><img src="https://github.com/sisatput/LearnPythonImg/blob/main/Week%203/Def.png" /></div>

- **Call**:

  - Call a function by using the function name followed by parentheses. You can pass arguments to the function if it requires input parameters.

    <div align="center"><img src="https://github.com/sisatput/LearnPythonImg/blob/main/Week%203/Call.png" /></div>

- **Return**:

  - Use the `return` statement to return a value from a function. The function will terminate and return the specified value.

    <div align="center"><img src="https://github.com/sisatput/LearnPythonImg/blob/main/Week%203/Return.png" /></div>

- **Pass by Reference vs Value**:

  - In Python, arguments are passed by reference, meaning the function receives a reference to the object in memory. Changes made to mutable objects (e.g., lists) within the function will affect the original object.
  - Unlike mutable objects, immutable objects (e.g., integers, strings) cannot be modified in place. If you reassign an immutable object within a function, it will create a new object in memory.

    <div align="center"><img src="https://github.com/sisatput/LearnPythonImg/blob/main/Week%203/Pass.png" /></div>

## NumPy

- NumPy is a powerful library for numerical computing in Python. It provides support for multidimensional arrays, mathematical functions, and linear algebra operations. NumPy is widely used in data analysis, machine learning, and scientific computing.
- To use NumPy, you need to import the library using the `import numpy as np` statement.

- **NumPy Array**:

  - A NumPy array is a grid of values with the same data type. It can be created using the `np.array()` function by passing a list or tuple of values.

    <div align="center"><img src="https://github.com/sisatput/LearnPythonImg/blob/main/Week%203/Narray.png" /></div>

- **Dimensions in Arrays**:

  - Dimensions in NumPy arrays refer to the number of axes or dimensions in the array. A 1D array has one axis, a 2D array has two axes, and so on. Uses `ndim` attribute to get the number of dimensions.

    <div align="center"><img src="https://github.com/sisatput/LearnPythonImg/blob/main/Week%203/Dimensions.png" /></div>

  - Customizing the number of dimensions in a NumPy array using the ndmin parameter.

    <div align="center"><img src="https://github.com/sisatput/LearnPythonImg/blob/main/Week%203/Dimensions%20Cus.png" /></div>

- **Get a Element From Array**:

  - Use indexing to access elements in a NumPy array. You can specify the row and column indices to retrieve a specific element.

    <div align="center"><img src="https://github.com/sisatput/LearnPythonImg/blob/main/Week%203/Element%20Indexing.png" /></div>

  - Get Element from Dimensional Array.

    <div align="center"><img src="https://github.com/sisatput/LearnPythonImg/blob/main/Week%203/Element%20Dimensional.png" /></div>

## Pandas

- Pandas is a popular data manipulation library built on top of NumPy. It provides data structures like Series and DataFrame, which are essential for working with structured data.
- To use Pandas, you need to import the library using the `import pandas as pd` statement.

### Pandas - Series

- A Pandas Series is a one-dimensional labeled array capable of holding data of any type. It is similar to a NumPy array but with additional indexing capabilities. pd.Series() function is used to create a Series.

    <div align="center"><img src="https://github.com/sisatput/LearnPythonImg/blob/main/Week%203/Pd%20Series.png" /></div>

- **Implicit and Explicit Indexing**:

  - By default, a Series is created with an implicit integer index starting from 0. You can specify custom labels for the index using the `index` parameter.

    - Explicit Indexing :
      Allows you to assign custom labels to the elements in a Series. You can use the `index` parameter to specify the index labels.

    <div align="center"><img src="https://github.com/sisatput/LearnPythonImg/blob/main/Week%203/Pd%20Explicit.png" /></div>

    - Implicit Indexing :
      Uses the default integer index to access elements in a Series. You can use the default index to retrieve values from the Series.

    <div align="center"><img src="https://github.com/sisatput/LearnPythonImg/blob/main/Week%203/Pd%20Implicit.png" /></div>

- **Data Slicing**:

  - Data slicing allows you to extract a subset of data from a Series based on the index labels or positions. You can use slicing to select specific elements or ranges of elements.

    - Explicit Indexing :
    <div align="center"><img src="https://github.com/sisatput/LearnPythonImg/blob/main/Week%203/Pd%20Ds%20Explicit.png" /></div>

    - Implicit Indexing :
    <div align="center"><img src="https://github.com/sisatput/LearnPythonImg/blob/main/Week%203/Pd%20Ds%20Implicit.png" /></div>

- **LOC and ILOC**:

  - The `loc` attribute is used to access data based on explicit index labels, while the `iloc` attribute is used to access data based on implicit integer positions.

    - LOC :
    <div align="center"><img src="https://github.com/sisatput/LearnPythonImg/blob/main/Week%203/LOC.png" /></div>

    - ILOC :
    <div align="center"><img src="https://github.com/sisatput/LearnPythonImg/blob/main/Week%203/ILOC.png" /></div>

  - **Dictionary to Series**:

    - You can convert a Python dictionary into a Pandas Series using the `pd.Series()` function. The keys of the dictionary become the index labels, and the values become the data elements.

      - Data Dictionary :
      <div align="center"><img src="https://github.com/sisatput/LearnPythonImg/blob/main/Week%203/Pd%20Series%20-%20Data%20Dictionary.png" /></div>

      - Data Series :
      <div align="center"><img src="https://github.com/sisatput/LearnPythonImg/blob/main/Week%203/Pd%20Series%20-%20Data%20Series.png" /></div>

### Pandas - DataFrame

- A Pandas DataFrame is a two-dimensional labeled data structure with columns of potentially different types. It is similar to a spreadsheet or SQL table and is widely used for data analysis and manipulation.

  - **Convert Data Series to DataFrame**:

  - You can convert a Pandas Series into a DataFrame using the `pd.DataFrame()` function. The Series elements become the data values in the DataFrame, and the index labels become the row labels.

    Data Frame :
    <div align="center"><img src="https://github.com/sisatput/LearnPythonImg/blob/main/Week%203/Data%20Frame%20-%20Series.png" /></div>

  - Accessing Data in DataFrame :

    - You can access data in a DataFrame using the column names. Use the column name as an index to retrieve the values in that column.

      <div align="center"><img src="https://github.com/sisatput/LearnPythonImg/blob/main/Week%203/Accessing%20Data%20Frame%20-%20Series.png" /></div>

  - **Load Data from CSV File**:

    - You can load data from a CSV file into a Pandas DataFrame using the `pd.read_csv()` function. Specify the file path as an argument to read the CSV file and create a DataFrame.

    - Data CSV Source : [Data Source](https://www.kaggle.com/datasets/shivamb/disney-movies-and-tv-shows)

    <div align="center"><img src="https://github.com/sisatput/LearnPythonImg/blob/main/Week%203/Load%20CSV.png" /></div>

  - **head()**:

    - The `head()` method is used to display the first few rows of a DataFrame. By default, it shows the first five rows, but you can specify the number of rows to display.

      <div align="center"><img src="https://github.com/sisatput/LearnPythonImg/blob/main/Week%203/head.png" /></div>

  - **info()**:

    - The `info()` method provides a concise summary of the DataFrame, including the data types, non-null values, and memory usage. It is useful for understanding the structure of the DataFrame.

      <div align="center"><img src="https://github.com/sisatput/LearnPythonImg/blob/main/Week%203/info.png" /></div>

  - **notnull()**:

    - The `notnull()` method returns a boolean mask indicating whether each value in the DataFrame is not null (i.e., contains a valid value). It is useful for filtering out missing data.

      <div align="center"><img src="https://github.com/sisatput/LearnPythonImg/blob/main/Week%203/notnull.png" /></div>

    - `notnull().sum()` used to count the number of non-null values in each column.

      <div align="center"><img src="https://github.com/sisatput/LearnPythonImg/blob/main/Week%203/notnull%20sum.png" /></div>

  - **isnull()**:

    - The `isnull()` method returns a boolean mask indicating whether each value in the DataFrame is null (i.e., missing or NaN). It is useful for identifying missing data in the DataFrame.

      <div align="center"><img src="https://github.com/sisatput/LearnPythonImg/blob/main/Week%203/isnull.png" /></div>

    - `isnull().sum()` used to count the number of missing values in each column.

      <div align="center"><img src="https://github.com/sisatput/LearnPythonImg/blob/main/Week%203/isnull%20sum.png" /></div>

  - **tail()**:

    - The `tail()` method is used to display the last few rows of a DataFrame. By default, it shows the last five rows, but you can specify the number of rows to display.

      <div align="center"><img src="https://github.com/sisatput/LearnPythonImg/blob/main/Week%203/tail.png" /></div>

  - **shape**:

    - The `shape` attribute returns a tuple representing the dimensions of the DataFrame (number of rows, number of columns). It is useful for understanding the size of the DataFrame.

      <div align="center"><img src="https://github.com/sisatput/LearnPythonImg/blob/main/Week%203/shape.png" /></div>

  - **columns**:

    - The `columns` attribute returns the column labels of the DataFrame. It is useful for accessing and manipulating the column names.

      <div align="center"><img src="https://github.com/sisatput/LearnPythonImg/blob/main/Week%203/columns.png" /></div>

  - **index**:

    - The `index` attribute returns the row labels of the DataFrame. It is useful for accessing and manipulating the row indices.

      <div align="center"><img src="https://github.com/sisatput/LearnPythonImg/blob/main/Week%203/index.png" /></div>

  - **describe()**:

    - The `describe()` method generates descriptive statistics for the numerical columns in the DataFrame, including count, mean, standard deviation, minimum, maximum, and quartile values.

      <div align="center"><img src="https://github.com/sisatput/LearnPythonImg/blob/main/Week%203/describe.png" /></div>

  - **mean()**:

    - The `mean()` method calculates the mean value for each column in the DataFrame. It is useful for computing the average value of numerical data.

      <div align="center"><img src="https://github.com/sisatput/LearnPythonImg/blob/main/Week%203/mean.png" /></div>

  - **median()**:

    - The `median()` method calculates the median value for each column in the DataFrame. It is useful for finding the middle value of numerical data.

      <div align="center"><img src="https://github.com/sisatput/LearnPythonImg/blob/main/Week%203/median.png" /></div>

  - **mode()**:

    - The `mode()` method calculates the mode value for each column in the DataFrame. It is useful for finding the most frequently occurring value in categorical data.

      <div align="center"><img src="https://github.com/sisatput/LearnPythonImg/blob/main/Week%203/mode.png" /></div>

  - **max()**:

    - The `max()` method returns the maximum value for each column in the DataFrame. It is useful for finding the highest value in numerical data.

      <div align="center"><img src="https://github.com/sisatput/LearnPythonImg/blob/main/Week%203/max.png" /></div>

  - **min()**:

    - The `min()` method returns the minimum value for each column in the DataFrame. It is useful for finding the lowest value in numerical data.

      <div align="center"><img src="https://github.com/sisatput/LearnPythonImg/blob/main/Week%203/min.png" /></div>

  - **unique()**:

    - The `unique()` method returns an array of unique values in a column of the DataFrame. It is useful for identifying distinct values in categorical data.

      <div align="center"><img src="https://github.com/sisatput/LearnPythonImg/blob/main/Week%203/unique.png" /></div>

    - `nunique()` used to count the number of unique values in a column.

      <div align="center"><img src="https://github.com/sisatput/LearnPythonImg/blob/main/Week%203/nunique.png" /></div>

  - **value_counts()**:

    - The `value_counts()` method returns the frequency of each unique value in a column of the DataFrame. It is useful for counting occurrences of different values.

      <div align="center"><img src="https://github.com/sisatput/LearnPythonImg/blob/main/Week%203/value_counts.png" /></div>

  - **Get Specified Columns**:

    - You can select specific columns from a DataFrame by passing a list of column names inside square brackets. This allows you to focus on the columns of interest.

      <div align="center"><img src="https://github.com/sisatput/LearnPythonImg/blob/main/Week%203/Specified%20Columns.png" /></div>

    - You can filter data from columns based on specific conditions. Use the conditional statement inside square brackets to extract rows that meet the criteria.

        <div align="center"><img src="https://github.com/sisatput/LearnPythonImg/blob/main/Week%203/Specified%20Columns%20-%20Filtered.png" /></div>

## datetime

- The `datetime` module in Python provides classes for manipulating dates and times. It allows you to work with dates, times, and time intervals, making it easier to handle temporal data in your programs.

- Example :
  Use `strftime()` method to format the date and time as a string. You can specify the format codes to customize the output.
    <div align="center"><img src="https://github.com/sisatput/LearnPythonImg/blob/main/Week%203/datetime.png" /></div>

## Random Library

- The `random` module in Python provides functions for generating random numbers. It is commonly used in simulations, games, and statistical applications where random values are required.

  Example of Random Library :
    <div align="center"><img src="https://github.com/sisatput/LearnPythonImg/blob/main/Week%203/Random.png" /></div>

## Text File - Open, Read, Close

- Reading and writing text files is a common task in Python programming. You can open a file, read its contents, and close the file once you're done. The `open()` function is used to open a file, and the `read()` method is used to read the file contents.

  - Open a File :
    <div align="center"><img src="https://github.com/sisatput/LearnPythonImg/blob/main/Week%203/Open.png" /></div>

  - Read File Contents :
    <div align="center"><img src="https://github.com/sisatput/LearnPythonImg/blob/main/Week%203/Read.png" /></div>

  - Close the File :
    <div align="center"><img src="https://github.com/sisatput/LearnPythonImg/blob/main/Week%203/Close.png" /></div>

## End Notes

As you conclude this part of our Python Mastery for Data Analysts guide, remember that Python is a versatile and powerful language extensively utilized across various fields, including data analysis, machine learning, and web development. By mastering foundational concepts like functions, NumPy, Pandas, datetime handling, the Random Library, and text file manipulation, you're equipping yourself with essential skills for real-world data analysis tasks.

This guide serves as a solid foundation for your Python journey, providing you with the necessary knowledge to continue building upon. Keep practicing, experimenting with different concepts, and working on projects to reinforce your understanding.

Keep up the great work, and may your learning journey be filled with success and discovery! 🚀
