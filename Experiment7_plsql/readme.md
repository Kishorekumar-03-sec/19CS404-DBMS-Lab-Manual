# Experiment 7: PL/SQL – Variables, Control Structures and Loops

## NAME: Kishorekumar S
## REG NO:212224040162
## DATE:18/05/2026

## AIM
To write and execute simple PL/SQL programs using variables, loops, and conditional statements.


## THEORY

PL/SQL, which stands for Procedural Language extensions to the Structured Query Language (SQL). It is a combination of SQL along with the procedural features of programming languages.

**Syntax:**
```sql
DECLARE 
   <declarations section> 
BEGIN 
   <executable command(s)>
EXCEPTION 
   <exception handling> 
END;
```

### Basic Components of PL/SQL Block:
- DECLARE: Section to declare variables and constants.
- BEGIN: The execution section that contains PL/SQL statements.
- EXCEPTION: Handles errors or exceptions that occur in the program.
- END: Marks the end of the PL/SQL block.

# PL/SQL Programs – Steps and Expected Output

## 1. Write a PL/SQL program to find the Greatest of Two Numbers

### Steps:
- Declare two numeric variables and initialize them.
- Use an `IF` statement to compare the values.
- Display the greater number using `DBMS_OUTPUT.PUT_LINE`.

**Expected Output:**  
Greater number is: 80

**Program**

      DECLARE
          a NUMBER := 80;
          b NUMBER := 45;
      BEGIN
          IF a > b THEN
              DBMS_OUTPUT.PUT_LINE('Greater number is: ' || a);
          ELSE
              DBMS_OUTPUT.PUT_LINE('Greater number is: ' || b);
          END IF;
      END;
      /

**Output**

<img width="938" height="379" alt="Screenshot 2026-05-18 155201" src="https://github.com/user-attachments/assets/0485ce85-de3e-4b79-95a0-b4a83940d5cb" />

---

## 2. Write a PL/SQL program to Calculate Sum of First N Natural Numbers

### Steps:
- Declare a variable `n` and assign a value (e.g., 10).
- Initialize a `sum` variable to 0.
- Use a `WHILE` loop to iterate from 1 to `n`, adding each number to the sum.
- Display the result using `DBMS_OUTPUT.PUT_LINE`.

**Expected Output:**  
Sum of first 10 natural numbers is: 55

**Program**
```
         DECLARE
             n NUMBER := 10;
             i NUMBER := 1;
             sum1 NUMBER := 0;
         BEGIN
             WHILE i <= n LOOP
                 sum1 := sum1 + i;
                 i := i + 1;
             END LOOP;
         
             DBMS_OUTPUT.PUT_LINE('Sum of first 10 natural numbers is: ' || sum1);
         END;
         /
```

**Output**

<img width="933" height="392" alt="Screenshot 2026-05-18 155721" src="https://github.com/user-attachments/assets/186f0196-783e-4525-9825-7b414adae6ca" />

---

## 3. Write a PL/SQL program to generate Fibonacci series

### Steps:
- Declare the variable `n` to indicate how many terms to generate.
- Initialize the first two Fibonacci numbers (0 and 1).
- Use a loop to generate the next terms using the formula `c = a + b`.
- Print each term in the series.

**Expected Output:**  
n = 7  
Fibonacci sequence: 0, 1, 1, 2, 3, 5, 8

**Program**
```
DECLARE
    n NUMBER := 7;
    a NUMBER := 0;
    b NUMBER := 1;
    c NUMBER;
    i NUMBER := 3;
BEGIN
    DBMS_OUTPUT.PUT_LINE('Fibonacci sequence:');

    DBMS_OUTPUT.PUT(a || ', ');
    DBMS_OUTPUT.PUT(b || ', ');

    WHILE i <= n LOOP
        c := a + b;
        DBMS_OUTPUT.PUT(c);

        IF i < n THEN
            DBMS_OUTPUT.PUT(', ');
        END IF;

        a := b;
        b := c;
        i := i + 1;
    END LOOP;
END;
/

```

**Output**

<img width="941" height="398" alt="Screenshot 2026-05-18 160237" src="https://github.com/user-attachments/assets/cbe404dc-e622-46fa-87ad-1790149f69cc" />

---

## 4. Write a PL/SQL Program to display the number in Reverse Order

### Steps:
- Declare a variable `n` and assign a value (e.g., 1535).
- Use a loop to extract each digit using modulo and reverse the number.
- Display the reversed number.

**Expected Output:**  
n = 1535  
Reversed number is 5351

**Program**
```
DECLARE
    n NUMBER := 1535;
    rev NUMBER := 0;
    rem NUMBER;
BEGIN
    WHILE n > 0 LOOP
        rem := MOD(n,10);
        rev := rev * 10 + rem;
        n := TRUNC(n/10);
    END LOOP;

    DBMS_OUTPUT.PUT_LINE('Reversed number is ' || rev);
END;
/
```

**Output**

<img width="895" height="390" alt="Screenshot 2026-05-18 160430" src="https://github.com/user-attachments/assets/583cb17e-4acb-4d44-930b-272f8671519d" />

---

## 5. Write a PL/SQL program to find the largest of three numbers

### Steps:
- Declare three numeric variables `a`, `b`, and `c`.
- Use nested `IF-ELSIF-ELSE` conditions to find the largest among the three.
- Display the largest number.

**Expected Output:**  
a = 10, b = 9, c = 15  
Largest of three number is 15

**Program**
```
DECLARE
    a NUMBER := 10;
    b NUMBER := 9;
    c NUMBER := 15;
BEGIN
    IF a > b AND a > c THEN
        DBMS_OUTPUT.PUT_LINE('Largest of three number is ' || a);

    ELSIF b > a AND b > c THEN
        DBMS_OUTPUT.PUT_LINE('Largest of three number is ' || b);

    ELSE
        DBMS_OUTPUT.PUT_LINE('Largest of three number is ' || c);
    END IF;
END;
/

```

**Output**

<img width="920" height="384" alt="Screenshot 2026-05-18 160704" src="https://github.com/user-attachments/assets/11249e85-1270-4dcc-bc8e-ee8126c08f06" />


## RESULT
Thus, the PL/SQL programs using variables, conditionals, and loops were executed successfully.
