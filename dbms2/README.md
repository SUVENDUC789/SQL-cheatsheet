# DBMS CLASS 2

## 1) DEETE ROW WITH SPECIFIC DOB:
```sql
DELETE FROM EMP WHERE DOB>='01-JUN-00' AND DOB<='30-JUN-00';
```

## 2) ALTER (ADD COLOUMN)
```sql
ALTER TABLE EMP ADD PANNO NUMBER(10);
```

## 3) UPDATE:
```sql
UPDATE EMP SET PANNO=456789 WHERE ID='EO4';

UPDATE EMP SET ID='E05' WHERE NAME='SUVENDU';

UPDATE EMP SET ID='E06' WHERE NAME='HRITIK';
```

## 4) ALTER (DROP COLOUMN)
```sql
ALTER TABLE EMP DROP COLUMN PANNO;
```

## 5) ALTER MODIFY COLUMN SIZE:
```sql
ALTER TABLE EMP MODIFY SALARY NUMBER(10);
```

## 6) SET PRIMARY KEY USING ALTER :
```sql
ALTER TABLE EMP ADD PRIMARY KEY(ID);
```

## 7) SET COMPOSITE KEY USING ALTER:
```sql
ALTER TABLE EMP ADD PRIMARY KEY(ID,NAME);
```


## 8) SELECT
```sql
SELECT * FROM EMP WHERE CITY='DUNLOP' OR CITY='PUNE';
SELECT * FROM EMP WHERE SALARY>=1800 AND SALARY<=20000;
```

## 9) BETWEEN:
```sql
SELECT * FROM EMP WHERE SALARY BETWEEN 1800 AND 20000;
```

## 10) IN :
```sql
SELECT * FROM EMP WHERE CITY IN ('DUNLOP','PUNE');
```

## 11) NOT IN :
```sql
SELECT * FROM EMP WHERE CITY NOT IN ('DUNLOP','PUNE');
```

## 12) LIKE:
```sql
SELECT * FROM EMP WHERE NAME LIKE 'S%';
SELECT * FROM EMP WHERE NAME LIKE '%S';
SELECT * FROM EMP WHERE NAME LIKE 'DEB%';
SELECT * FROM EMP WHERE NAME LIKE '_U%';
SELECT * FROM EMP WHERE NAME LIKE '__B%';
SELECT * FROM EMP WHERE NAME LIKE '%U%';
SELECT * FROM EMP WHERE NAME LIKE '_%A%_';
```
## 13) NOT LIKE:
```sql
SELECT * FROM EMP WHERE NAME NOT LIKE 'A%' AND NAME LIKE '%A%';
```

## 14) TEMPORARY NAME PROVIDE COLUMN:
```sql
SELECT (NAME||CITY) "DEVOLOPER NAME" FROM EMP;
```

## 15) PROVIDE SPACE:
```sql
SELECT (NAME||' '||CITY) "DEVOLOPER NAME" FROM EMP;
```

## 16) AS:
```sql
SELECT (NAME||' '||CITY) AS "DEVOLOPER NAME" FROM EMP;

```
## 17) MAX:
```sql
SELECT MAX(SALARY) AS SAL FROM EMP;
```
## 18)MIN:
```sql
SELECT MIN(SALARY) AS SAL FROM EMP;
```


## 19) AVG:
```sql
SELECT AVG(SALARY) AS SAL FROM EMP;
```


## 20) SUM:
```sql
SELECT SUM(SALARY) AS SAL FROM EMP;
```


## 21)COUNT:
```sql
SELECT COUNT(*) FROM EMP;
SELECT COUNT(ID) FROM EMP;
```

## 22) SQRT DUAL:
```sql
SELECT SQRT(250) FROM DUAL;
SELECT SQRT(25) FROM DUAL;
```

## 23) ABS:
```sql
SELECT ABS(-250) FROM DUAL;
```

## 24) SYSDATE:
```sql
SELECT SYSDATE FROM DUAL;
```

## 25) TRUNC: (FLOAT->INT)
```sql
SELECT TRUNC((SYSDATE-DOB)/365) AS "AGE" FROM EMP;
```

## 26) FIND MAXIMUM AGE:
```sql
SELECT MAX(TRUNC((SYSDATE-DOB)/365)) AS "MAX-AGE" FROM EMP;
```

## 27)FIND MINIMUM AGE:
```sql
SELECT MIN(TRUNC((SYSDATE-DOB)/365)) AS "MAX-AGE" FROM EMP;
```