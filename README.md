import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

df = pd.read_csv(r'C:\Users\Tringapps-User21\Downloads\house\housing.csv')  

sns.heatmap(df.corr(),annot=True,cmap='RdYlGn',linewidths=0.2) 
fig=plt.gcf()
fig.set_size_inches(20,12)
plt.show()

df.head()
df1=pd.DataFrame(df)
place=df1['ocean_proximity']
price=df1['median_house_value']
fig=plt.figure(figsize=(10,7))
plt.bar(place,price)
plt.show()
