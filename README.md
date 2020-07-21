# mnist_dataset


 installing requirements: conda install -c conda-forge mnist

sample python code for accessing the dataset :

    from mnist import MNIST

    mndata = MNIST(r'C:\Users\krish\OneDrive\Documents\krishna\sem6\DL\mnist')

    mndata.gz = True
 
    train_images = np.zeros([1000,28,28])

    test_images = np.zeros([1000,28,28])


    images_tr,train_labels = mndata.load_training()

    images_tr = np.array(images_tr[:1000])

    train_labels = np.array(train_labels[:1000])

    images_ts1,test_labels = mndata.load_testing()

    images_ts = np.array(images_ts1[:1000])

    test_labels = np.array(test_labels[0:1000])


    for i in range(1000):

       train_images[i] = images_tr[i].reshape(28,28) 

       test_images[i] = images_ts[i].reshape(28,28)

