# Image-Cartoonification-using-K-Means-Clustering

This project has been a result of studying a conference paper "A Novel Method of Transforming Real Images & Videos into Cartoon Images & Videos" and it's practical implementation.

cite as - 
Moizuddin, Enayat, S., Khan, I.R. (2022). A Novel Method of Transforming Real Images & Videos into Cartoon Images & Videos. In: Chen, J.IZ., Tavares, J.M.R.S., Iliyasu, A.M., Du, KL. (eds) Second International Conference on Image Processing and Capsule Networks. ICIPCN 2021. Lecture Notes in Networks and Systems, vol 300. Springer, Cham. https://doi.org/10.1007/978-3-030-84760-9_61

The process of creating a cartoon effect of an image can be initially branched into 2 divisions – 1)Reduction of color palette

2)	Highlighted Edges.

REDUCTION OF COLOR PALETTE

The most important task is to minimize the color regions and apply cartoon features. Through this method, the colors are minimized on multiple filters so as to create an equal color region.

1.	BILATERAL FILTERING- The important aspect of this filter is to smooth the images without creating any sort of noise also while preserving the edges. Filtering is performed by reading an image in a file and storing the image in a matrix object. Firstly creating an empty matrix to store the result and applying a bilateral filter. The nature of the filter totally depends on the kernel size and testing by running many iterations.



2.	GAUSSIAN BLUR- It is a widely used effect in image processing, typically to reduce image noise and minimize detail. Gaussian smoothing is used as a initial process in computer vision algorithms with the intention to improve image structures at different scales.

HIGHLIGHTED EDGES

Figuring out a smooth outline that represents or bounds image shape is an important property to receive a quality image. All Edge processing tasks done here are:

1.	MEDIAN BLUR – In the process of smoothing the image a blur effect is applied. This is done with the help of the median Blur() function. Here the center pixel is made to assign a mean value which is the mean of all the pixels existing under the kernel. It also helps to remove noise in the image.
 


2.	ADAPTIVE THRESHOLD - In this step we try to retrieve edges and highlight them. This is carried out by adaptive threshold. The threshold value is the mean value of surrounding pixel values that comes under a single block minus constant c. c is constant that is to be subtracted from the mean of surrounding neighborhood pixels.



Combine reduction of color palette and highlighted edges image:- The final task is done by masking where we perform bit wise and on the highlighted edges and the smooth colors. With this we get a cartoon image.

K MEANS CLUSTERING

K-means clustering is one of the algorithms which unsupervised machine learning supports hence before moving forward with K-means let’s have background knowledge of the unsupervised learning method. In this method, we don’t have predefined labels unlike the supervised method hence we don’t draw predictions but make clusters/groups out of them so that the data could get segmented according to the features that are fed to the model.


 
 



As discussed, this algorithm is a part of unsupervised learning so instead of making predictions we will segment that data based on the different number of clusters. K-means follow a few mathematical steps which are important to discuss:

Step 1: Select the number of clusters, and there are a few ways to select the appropriate number of clusters like the elbow method and domain knowledge.

Step 2: Assigning the K points or we can also say randomly assigning the centroids from the dataset.

Step 3: In the last step each K point will be adjusted closely towards its closest centroid that will eventually form the clusters/group.


