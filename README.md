# 01.26-Week_13_Project-3-Suganthan_Thamotharampillai




Exploratory Data Analysis
-------------------------

```
# RATING
plt.figure(facecolor='#eaeaf2'); sns.set(rc = {'figure.figsize':(10,5)});
sns.countplot(data=df, x=df['certification'], palette = "twilight").set(title='\nR A T I N G\n');
```

![png](Files/ReadMe/EDA1.png)


```
# REVENUE
plots = sns.barplot(x="certification", y="revenue", data=df, palette = "rocket", errorbar=None);
for bar in plots.patches:
    plots.annotate(format(str(round(bar.get_height()/1000000))+'million'),
                   (bar.get_x() + bar.get_width() / 2,
                    bar.get_height()), ha='center', va='center',
                   size=12, xytext=(0, 8),
                   textcoords='offset points');plt.title("\nR E V E N U E\n")
```

![png](Files/ReadMe/EDA2.png)


```
# BUDGET
plot = sns.barplot(x="certification", y="budget", data=df, palette = "mako", errorbar=None); 
for bar in plot.patches:
    plot.annotate(format(str(round(bar.get_height()/1000000))+'million'),
                   (bar.get_x() + bar.get_width() / 2,
                    bar.get_height()), ha='center', va='center',
                   size=12, xytext=(0, 8),
                   textcoords='offset points');plt.title("\nB U D G E T\n")
```

![png](Files/ReadMe/EDA3.png)

![png](Files/ReadMe/EDA4.png)