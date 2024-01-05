import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv('/content/dataset - netflix1 (3).csv')
print(df.head())
plt.figure(figsize=(12,6))
plt.subplot(1,2,1)
sns.countplot(x='type',data=df,palette='viridis')
plt.title('count of movies and tv shows')
plt.subplot(1,2,2)
sns.barplot(x='release_year',y='duration',data=df,palette='Set2')
plt.title('release year vs duration')
plt.tight_layout()
plt.show()
