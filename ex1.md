##PROBLEM 1:
```
def display_samples():
    count = 0	
    for image in os.listdir("notMNIST_large/A"):
        if(count < 2):
            display(Image(os.path.join("notMNIST_large/A", image)))
            count += 1
display_samples()
```

##PROBLEM 2:
```
%matplotlib inline

def display_problem2():
    image = train_datasets[0]
    set = pickle.load(open(image))
    plt.imshow(set[0])
    plt.show()
display_problem2()
```

##PROBLEM 3:
```
def display_problem2():
    image = train_datasets[0]
    for i in xrange(len(train_datasets)):
        print (pickle.load(open(train_datasets[i])).shape)
display_problem2()
```

##PROBLEM 4:
overlap = np.intersect1d(train_dataset, valid_dataset)
print ("This is the overlap: ", len(overlap))

##PROBLEM 5:
```
clf = LogisticRegression()

nsamples, nx, ny = train_dataset.shape
twoD_train_dataset = train_dataset.reshape((nsamples,nx*ny))


nsamples1, nx, ny = valid_dataset.shape
twoD_valid_dataset = valid_dataset.reshape((nsamples1,nx*ny))

print(twoD_train_dataset.shape, twoD_valid_dataset.shape)
clf.fit(twoD_train_dataset, train_labels)
```