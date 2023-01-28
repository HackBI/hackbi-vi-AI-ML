# AI/ Machine Learning Cheat Sheet

### Import statements

| Pandas import | import pandas as pd  |
| --- | --- |
| sklearn import | from sklearn import datasets |
| installing pandas | !pip install pandas |

### Panda DataFrames

🔹Check out the panda DataFrames api for more: [https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.html](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.html)

| Importing data from URL | data_url = “http://link goes here” <br> df = pd.read_csv(data_url) |
| --- | --- |
| Get first 5 rows of DataFrame | df.head() |
| Get first n rows of DataFrame | df.head(n) |
| get the header and data type for each column and the number of non-null values | df.info() |
| Get basic statistical data, such as mean, standard deviation, and percentiles, for all columns with numerical data types (i.e. integers and floats). | df.describe() |
| Get the labels or indices for the rows | df.index |
| Get the data types for each column | df.dtypes |
| Get the number of dimensions | df.ndim |
| Get the number of elements | df.size |
| Get the number of rows and columns | df.shape |

### matplotlib graphing

🔹Check out the matplotlib api for more: [https://matplotlib.org/stable/api/index.html](https://matplotlib.org/stable/api/index.html)

| Show your plot
(This needs to be called to actually see any visualization) | plt.show() |
| --- | --- |
| Give your plot a title | plt.title("Plot Title") |
| Give your x-axis a label | plt.xlabel("Label Name") |
| Give your y-axis a label | plt.ylabel("Label Name") |
| Add a grid to your plot | plt.grid() |
| Add a legend to your plot. 
(You must add labels to each plot for this to do anything) | plt.legend() |
| Changing the text size for any title, labels, etc. 
(ex: small, large, x-large) | plt.title(…, fontsize = 'size') |
| Changing the text style for any title, labels, etc. 
(ex: normal, italic, oblique) | plt.title(…, style = 'options') |
| Changing the text family/font for any title, labels, etc. 
(ex: cursive, fantasy, serif, monospace) | plt.title(…, family = 'font') |
| Changing the text location for any title, labels, etc. 
(ex: left, right, bottom, top) | plt.title(…, loc = 'location') |
| Changing the text weight for any title, labels, etc. 
(ex: normal, regular, medium, bold, heavy, extra bold) | plt.title(…, fontweight = 'options') |
| Change the size of the whole figure. 
(Must come before you plot anything) | plt.figure(figsize = (width,height)) |
| Change the background color of the figure. | plt.figure(facecolor = 'c') |
| Change the border color of the figure. | plt.figure(edgecolor = 'c') |

### Scatterplots(matplotlib)

🔹scatterplot api: [https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.scatter.html](https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.scatter.html)

| Create a scatter plot | plt.scatter(x_var, y_var) |
| --- | --- |
| Assigning a label to this data set for a legend. | plt.scatter(x_var, y_var, label = 'text')
plt.legend() |
| Change the color of all data points the same way. | plt.scatter(x_var, y_var, color = 'c') |
| Change the color of each data point differently. 
Each element of the list must be a valid color option. | plt.scatter(x_var, y_var, color = ['c1',…] |
| Change the transparency of the data points. 
t can take values from 0 (transparent) to 1 (opaque). | plt.scatter(x_var, y_var, alpha = t) |
| Change the marker style of the data points. | plt.scatter(x_var, y_var, marker = 'm') |
| Change the size of all data points in the same way. 
s can be any number (int or float) above 0. | plt.scatter(x_var, y_var, size = s) |
| Change the size of each data point differently. Provide a list of sizes, one for each data point. | plt.scatter(x_var, y_var, size = [s1,…]) |

### KNN

🔹KNN w/ sklearn api: [https://scikit-learn.org/stable/modules/generated/sklearn.neighbors.KNeighborsClassifier.html](https://scikit-learn.org/stable/modules/generated/sklearn.neighbors.KNeighborsClassifier.html)

| Splitting dataset into: <br>
X_train: training data inputs <br>
X_test: testing data inputs <br>
y_train: training data outputs <br>
y_test: testing data outputs <br>
<br>
from: <br>
inputs: data of our chosen features <br>
output: data of our chosen label/class <br>
<br>
with:  <br>
test_size: the fraction of the dataset that you want to use for testing (usually 0.2) <br>
random_state = any int you want is fine. The same number will produce the same split every time. | X_train, X_test, y_train, y_test = train_test_split(inputs, output, test_size = 0.2, random_state = 42) |
| --- | --- |
| initialize a KNN Classifier, setting k (here k = 3) | model= KNeighborsClassifier(n_neighbors= 3) |
| Train your model on the training dataset | model.fit(x_train, y_train) |
| Use your trained model to make predictions from the test data inputs. 
(This returns a list of predictions, even if you just asked for a single prediction) | pred = model.predict(x_test) |
