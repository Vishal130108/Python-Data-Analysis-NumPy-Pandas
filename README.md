# Python Data Analysis — NumPy & Pandas

### Assignment Overview

This assignment focuses on applying **NumPy and Pandas** for fundamental data analysis tasks using temperature and transaction datasets. The analysis covers numerical computations, data inspection, indexing, slicing, filtering, aggregation, and data manipulation.

---

# 1. NumPy Array Operations

## 1.1 Week 1 Temperature Array

### Result

    [22.5 25.3 20.8 23.4 26.1 24.8 21.9]

---

## 1.2 Array Properties

| Property | Result |
|---|---:|
| Shape | `(7,)` |
| Data Type | `float64` |
| Number of Elements | `7` |

---

## 1.3 Temperature Analysis

### Fahrenheit Conversion

    [72.5  77.54 69.44 74.12 78.98 76.64 71.42]

### Weekly Temperature Statistics

| Metric | Temperature (°C) |
|---|---:|
| Maximum | 26.1 |
| Minimum | 20.8 |
| Mean | 23.542857142857142 |

---

## 1.4 Array Indexing and Slicing

### First Three Days

    [22.5 25.3 20.8]

### Weekend Temperatures

    [24.8 21.9]

### Middle Three Days

    [20.8 23.4 26.1]

---

# 2. Two-Week Temperature Analysis

## 2.1 Two-Dimensional Temperature Array

### Result

    [[22.5 25.3 20.8 23.4 26.1 24.8 21.9]
     [19.2 22.5 21.3 24.  23.5 22.8 20.1]]

---

## 2.2 Two-Dimensional Array Properties

| Property | Result |
|---|---:|
| Shape | `(2, 7)` |
| Data Type | `float64` |
| Total Elements | `14` |

---

## 2.3 Weekly Temperature Extraction

### Week 1

    [22.5 25.3 20.8 23.4 26.1 24.8 21.9]

### Week 2

    [19.2 22.5 21.3 24.  23.5 22.8 20.1]

### Week 1 Weekend

    [24.8 21.9]

### Week 2 Weekend

    [22.8 20.1]

---

# 3. Pandas Series

## 3.1 Marks Series

### Result

    Rank1    95
    Rank2    92
    Rank3    89
    Rank4    85
    Rank5    80
    dtype: int64

---

## 3.2 Series Indexing and Filtering

### 1st Rank — Integer Index Position

    95

### Top 3 Ranks — Label-Based Selection

    Rank1    95
    Rank2    92
    Rank3    89
    dtype: int64

### 3rd Rank — Position-Based Selection

    89

### Marks Greater Than 90

    Rank1    95
    Rank2    92
    dtype: int64

---

## 3.3 Series Manipulation

### Updated Marks

    Rank1    100
    Rank2     92
    Rank3     89
    Rank4     85
    dtype: int64

### Calculated CGPA

    Rank1    10.0
    Rank2     9.2
    Rank3     8.9
    Rank4     8.5
    dtype: float64

---

# 4. Pandas DataFrame

## 4.1 Transaction Dataset

| TransactionID | ProductCategory | Region | Amount |
|---:|---|---|---:|
| 101 | Electronics | North | 200 |
| 102 | Clothing | South | 150 |
| 103 | Electronics | North | 300 |
| 104 | Furniture | East | 450 |
| 105 | Clothing | West | 200 |
| 106 | Electronics | North | 250 |
| 107 | Furniture | East | 300 |
| 108 | Clothing | West | 180 |
| 109 | Furniture | South | 350 |
| 110 | Electronics | North | 400 |

---

# 5. Data Exploration

## 5.1 First Five Transactions

| TransactionID | ProductCategory | Region | Amount |
|---:|---|---|---:|
| 101 | Electronics | North | 200 |
| 102 | Clothing | South | 150 |
| 103 | Electronics | North | 300 |
| 104 | Furniture | East | 450 |
| 105 | Clothing | West | 200 |

---

## 5.2 Last Five Transactions

| TransactionID | ProductCategory | Region | Amount |
|---:|---|---|---:|
| 106 | Electronics | North | 250 |
| 107 | Furniture | East | 300 |
| 108 | Clothing | West | 180 |
| 109 | Furniture | South | 350 |
| 110 | Electronics | North | 400 |

---

## 5.3 DataFrame Structure

### Shape

    (10, 4)

### Columns

    TransactionID
    ProductCategory
    Region
    Amount

### Data Types

    TransactionID        int64
    ProductCategory     object
    Region              object
    Amount               int64

---

## 5.4 Product Category and Amount

| ProductCategory | Amount |
|---|---:|
| Electronics | 200 |
| Clothing | 150 |
| Electronics | 300 |
| Furniture | 450 |
| Clothing | 200 |
| Electronics | 250 |
| Furniture | 300 |
| Clothing | 180 |
| Furniture | 350 |
| Electronics | 400 |

---

## 5.5 Last Three Columns

| ProductCategory | Region | Amount |
|---|---|---:|
| Electronics | North | 200 |
| Clothing | South | 150 |
| Electronics | North | 300 |
| Furniture | East | 450 |
| Clothing | West | 200 |
| Electronics | North | 250 |
| Furniture | East | 300 |
| Clothing | West | 180 |
| Furniture | South | 350 |
| Electronics | North | 400 |

---

## 5.6 North Region Transactions Above 200

| TransactionID | ProductCategory | Region | Amount |
|---:|---|---|---:|
| 103 | Electronics | North | 300 |
| 106 | Electronics | North | 250 |
| 110 | Electronics | North | 400 |

---

## 5.7 Product Category Distribution

| Product Category | Transaction Count |
|---|---:|
| Electronics | 4 |
| Clothing | 3 |
| Furniture | 3 |

---

## 5.8 Unique Regions

    North
    South
    East
    West

---

## 5.9 Average Transaction Amount by Region

| Region | Mean Amount |
|---|---:|
| East | 375.0 |
| North | 287.5 |
| South | 250.0 |
| West | 190.0 |

---

# 6. DataFrame Manipulation

## 6.1 Transaction Amount Update

The amount for **TransactionID 102** was updated from `150` to `165`.

### Result

| TransactionID | Amount |
|---:|---:|
| 102 | 165 |

---

## 6.2 Discount Calculation

A **10% discount** was calculated based on the transaction amount.

| TransactionID | Amount | Discount |
|---:|---:|---:|
| 101 | 200 | 20.0 |
| 102 | 165 | 16.5 |
| 103 | 300 | 30.0 |
| 104 | 450 | 45.0 |
| 105 | 200 | 20.0 |
| 106 | 250 | 25.0 |
| 107 | 300 | 30.0 |
| 108 | 180 | 18.0 |
| 109 | 350 | 35.0 |
| 110 | 400 | 40.0 |

---

## 6.3 Transaction Removal

TransactionID **109** was removed from the DataFrame.

---

## 6.4 Final Transaction Dataset

| TransactionID | ProductCategory | Region | Amount |
|---:|---|---|---:|
| 101 | Electronics | North | 200 |
| 102 | Clothing | South | 165 |
| 103 | Electronics | North | 300 |
| 104 | Furniture | East | 450 |
| 105 | Clothing | West | 200 |
| 106 | Electronics | North | 250 |
| 107 | Furniture | East | 300 |
| 108 | Clothing | West | 180 |
| 110 | Electronics | North | 400 |

---

# 7. Skills and Concepts Covered

- NumPy 1D and 2D arrays
- Array properties and numerical operations
- Temperature conversion
- Statistical calculations
- Indexing and slicing
- Pandas Series creation and manipulation
- Label-based and position-based indexing
- Boolean filtering
- Pandas DataFrame creation
- Data inspection and exploration
- Column and row selection
- Value counts and unique values
- GroupBy and aggregation
- DataFrame filtering and modification
- Column creation and deletion

---

# 8. Conclusion

This assignment provided practical experience in using **NumPy and Pandas for structured data analysis**. The exercises covered the complete flow from creating and inspecting data to performing transformations, filtering records, calculating summary statistics, and manipulating tabular datasets.

Through the temperature analysis, NumPy was used for **numerical computation, array operations, indexing, and slicing**. The transaction analysis demonstrated how Pandas can be used for **data exploration, conditional filtering, aggregation, and structured DataFrame manipulation**.

Overall, the assignment strengthened the practical understanding of **Python-based data handling and analysis workflows**, providing a foundation for working with real-world datasets in data analytics.

---

## Tools & Technologies

**Python | NumPy | Pandas | Jupyter Notebook**

---
