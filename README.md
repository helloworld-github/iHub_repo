import numpy as np
import pandas as pd
import matplotlib.pyplot as pt

dataset=pd.read_csv("filename")
x=dataset.iLock[:,[2,3]].values
y=dataset.ilock[:,4].values
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.25)
from sklearn.preprocessing import StandardScaler
sc=StandardScaler()
x_train=sc.fit_transform(x_train)
x_test=sc.transform(x_test)
from sklearnneighbors inport KNeighborsClassifier
classifier=KNeighborsClassififier(n_neighbors=5,metric='minkowski')

classifier help to build the model.
classifier.fit(x_train,y_train)
y_pred=classifier.predict(x_test)

#to print
y_pred

#finding accuracy of model...

from sklearn.metric import confusion_matrix
cm=confusion_matrx(y_test,y_pred) 

===========================================working============

import pandas as pd
import numpy as np
import matplotlib.pyplot as pt
dataset=pd.read_csv("social_media_file.csv")
dataset.shape
x=dataset.iloc[:,[2,3]].values
x
y=dataset.iloc[:,4].values
y
from sklearn.model_selection import train_test_split

x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.25)
x_train.shape
y_train
x_test.shape
from sklearn.preprocessing import StandardScaler
sc=StandardScaler()
x_train=sc.fit_transform(x_train) #normalizingthe x_train value
x_train.shape
x_test=sc.transform(x_test)
x_test.shape
from sklearn.neighbors import KNeighborsClassifier
classifier=KNeighborsClassifier(n_neighbors=5,metric='minkowski')
classifier.fit(x_train,y_train)
y_pred=classifier.predict(x_test)
y_pred

#finding accuracy of model

from sklearn.metrics import confusion_matrix
cm=confusion_matrix(y_test,y_pred)
cm

#print((61+30)/(62+3+5+30))
