import pandas as pd
import numpy as np
import matplotlib.pyplot as plt

excel_file1 = 'E:\Ticket Details 1.xlsx'
excel_file2 = 'E:\Ticket Details 2.xlsx'
excel_file3 = 'E:\Ticket Details 3.xlsx'

df1 = pd.read_excel(excel_file1)
df2 = pd.read_excel(excel_file2)
df3 = pd.read_excel(excel_file3)

print(df1)

dfall = pd.concat([df1,df2,df3])
print(dfall)

dfall.plot(kind='bar')
plt.show

dfall.to_excel("output.xlsx")
