# PG Admission Predictor using Linear Regression in Java

### Java Mini Project: II Year Sem 3 CSE C

The classes (within their respective packages) are in "./Mini Project/build/classes"

(i) Classes and Packages:

1. Arrays
	Interface:
		ArrayType - for methods common to both Matrix and Vector
	Classes:	
		Matrix - for matrix operations in Linear Regression
		Vector - for vector operations in Linear Regression

2. Data
	Classes:
		LoadData - class with function to load data from the csv file into a 2D array.
3. Linear Regression
	Classes:
		Model - The class to train the Linear Regression model on the graduate admissions data, the trained parameters are obtained here.
4. Predictor
	Classes:
		Predictor - It has a static function to directly predict the chance of admission given an input array. The trained parameters are directly set it an array (to ensure they need not be trained again every time a prediction is needed).

(ii) GUI Classes:

	MainWindow - This class has all the functionality to create the GUI as well as handle exceptions

(iii) Exception Classes:

	GREException    - for invalid GRE Scores
	RESEXPException - for invalid Research Experience Values
	TOEFLEXception	-  for invalid TOEFL Scores
	CGPAException   - for invalid CGPA Values

(iv) The MainWindow class (MainWindow.java) has the main function in it and the entire project can be run as follows:

	1. Open a terminal in 'dist' directory
	2. Type: java -jar "Java Mini Project" to run the application

(v) OOPS Concepts used:

1. Classes and Interfaces - Interface: ArrayType
2. Inheritance - Custom Exception Classes inherit Exception
3. Overloading - sum() and sum(int) in Matrix  
4. Overriding - Custom Exception Classes override toString in Exception
5. Polymorphism (from 3 and 4)
6. Abstraction - Matrix/Vector methods are directly called in Model.java without their implementation being known.

(vi) Java Specific Concepts:

1. Custom Exception Classes (in MainWindow class)
2. Static methods and members (in Predictor class)
3. Collections Framework - ArrayList (in Model.java)
4. Generics (Double as type parameter in ArrayList)
5. GUI in NetBeans IDE

(vii) Team Members Info:

	1. Shashanka Venkatesh - 185001145
	2. Siddharth Sriraman  - 185001150
	3. Sreedhar V 	       - 185001161

(viii) Notes:

1. The dataset we used to train the model is in the main project directory (as a .csv file) and was taken from [Kaggle](https://www.kaggle.com/mohansacharya/graduate-admissions).

2. For actual running and deployment of the project, only the 'dist' directory and steps in (iv) are needed (all other directories are purely NetBeans and project related).

3. We have used java (JDK and JRE) version 1.8.0_172 to compile and run the project as newer versions are not supported in NetBeans 8.2.

4. If there are package locating problems while compiling the classes individually, mention the classpath in the javac command as follows:
      javac -cp './Mini Project/build/classes' file.java
