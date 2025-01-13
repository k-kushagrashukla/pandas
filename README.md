![Screenshot 2025-01-13 170158](https://github.com/user-attachments/assets/fc3c0bc7-4a02-4e1a-8e3d-0f8447b8f3bd)

# Pandas
pandas is a powerful and popular python library designed for data manipulation and for data analysis, it simplifies working with structured datasets like tables, spreadsheets or time series data.
## data manipulation
changing,organizing,or preparing data to make it useful and easier to understand
## data analysis
extracting trends, patterns and insights from the data to solve problems

![Screenshot 2025-01-13 170642](https://github.com/user-attachments/assets/4cff2064-1b89-49b3-bbd6-0679e8e23275)

![Screenshot 2025-01-13 170759](https://github.com/user-attachments/assets/5a3ba0f5-ec36-47b7-a6c8-5fa46f8b13ee)
---

```python
#for reading data frame
import pandas as pd
#df=pd.read_csv("sales_data_sample.csv",encoding="latin1")
#print(df)

#df=pd.read_excel("SampleSuperstore.xlsx")
df=pd.read_json("sample_Data.json")
print(df)
```

```python
#for getting info about dataframe
import pandas as pd
df=pd.read_json("sample_data.json")
print("displaying the info of dataset")
print(df.info())
```
```python
import pandas as pd
data={
    "name":['kushagra','niharika','stuti','shradhha','anjali'],
    "age":[10,20,30,40,50],
    "salary":[10000,140000,15000,3847,2000],
    "performance score":[85,70,90,92,23]
}

df=pd.DataFrame(data)
print("sample dataframe")
print(df)
print("names (single column return series)")
#selecting single column from table or data
name=df['name']
print(name)

#selecting  multiple columns
subset=df[["name","salary"]]
print('subset with name salary')
print(subset)
```

```python
import pandas as pd
data={
    "name":['kushagra','niharika','stuti','shradhha','anjali'],
    "age":[10,20,30,40,50],
    "salary":[10000,140000,15000,3847,2000],
    "performance score":[85,70,90,92,23]
}

df=pd.DataFrame(data)
high_salary =df[df['salary']>50000]
print('employees with salary >50000')
print(high_salary)


#filtering rows salary > 50k & age >20
filtered =df[(df['age']>10) & (df['salary']> 50000)]
print(f'employees list age >30+ salary>50000')
print(filtered)

#using or condition
filtered_or=df[(df['age']>35) | (df["performance score"]>90)]
print("employees older than 30 or performance score >90 ")
print(filtered_or)
```
```python
# for getting rows and columns using shape and column
import pandas as pd
data={
    "name":['kushagra','niharika','stuti','shradhha','anjali'],
    "age":[10,20,30,40,50],
    "salary":[10000,140000,15000,3847,2000],
    "performance score":[85,70,90,92,23]
}

df=pd.DataFrame(data)
print(df)
print(f'shape: {df.shape}')
print(f'column: {df.columns}')
```
