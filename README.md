# machinelearning-assignment-3--clustering-and-dimension-reduction-solved
**TO GET THIS SOLUTION VISIT:** [MachineLearning Assignment 3 -Clustering and Dimension Reduction Solved](https://www.ankitcodinghub.com/product/machinelearning-assignment-3-clustering-and-dimension-reduction-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;90959&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;0&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;0&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;0\/5 - (0 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;MachineLearning Assignment 3 -Clustering and Dimension Reduction&nbsp;Solved&quot;,&quot;width&quot;:&quot;0&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 0px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            <span class="kksr-muted">Rate this product</span>
    </div>
    </div>
<div class="page" title="Page 1">
<div class="section">
<div class="layoutArea">
<div class="column">
&nbsp;

In this assignment you will get familiar with some common techniques used in clustering of data and its analysis.

A. Dataset Preparation:

Download the Religious Texts Dataset from ​here​(also to be uploaded on Moodle). Use the Labelled​ dataset for this assignment. The dataset contains the ​Document Term Matrix​(DTM) from 8 different Religious Texts.

<ol>
<li>The first column contains the names of the religious text and their corresponding chapters. Replace the labels with only the names of the religious text (remove the chapter numbers, for eg., “Buddhism_Ch1” should become “Buddhism”). These are the class labels, and there are 8 of them. The rest of the columns represent the term frequency (frequency of the corresponding terms in the documents). ​The 14th row in the data (index 13 when you start at 0), “Buddhism_Ch14” is all zeros, because the original text is empty. Remove this row from the data and adjust the indices accordingly.</li>
<li>Now we want to convert the DTM to a ​TF-IDF​matrix. ​Note: Do NOT use the text provided in the corpus for computation of TF-IDF.To calculate the TF-IDF value of a term ‘t’ in the document ‘d’, use tf-idf (​ d, t) = ​tf ​(t, d) x ​idf ​(t),where t​f (​t, d) represents the term frequency of the term in the document (as given in the DTM), and i​df​(t) represents the inverse document frequency of the term.
Use i​df (​ t) = log [ (1 + n) / (1 + ​df ​(t)) ],​ where n is the total number of documents, and df(t) represents the document frequency (number of documents in which the term is present).

Finally we consider each document as a vector of TF-IDF scores for the different terms. Normalize each vector by dividing it with the length of the vector (L2 norm).

You can use ​scikit-learn​(or any equivalent library in other programming languages) to obtain this TF-IDF matrix.
</li>
</ol>
</div>
</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="section">
<div class="layoutArea">
<div class="column">
We define the similarity between two vectors by their cosine similarity, which is equivalent to the dot product of the two unit normalized vectors. ​For this assignment, consider the ​distance between two vectors as the negative exponential of their cosine similarity (​NOT​ the Euclidean

distance). ​Thus if the cosine similarity of two vectors is z, the distance is ​e(​ -z)

B. Agglomerative Clustering:

Implement a hierarchical agglomerative clustering algorithm, to obtain 8 clusters of documents. Use the ​single linkage​strategy to join clusters. ​Note: Do NOT use any ML library for this part.

Print the clusters into a file named ‘​agglomerative.txt’​ in the following format: Each line will represent a different cluster, and will contain a sorted comma separated list of the indices of the data points in that cluster. Sort the clusters by the minimum index of the data points present in that cluster.

Eg: if suppose you obtain clusters [1,3,5], [2], [4,0], then print out:

0,4

1,3,5

2

Here the numbers represent the index of the corresponding documents in the dataset (excluding the header).

C. KMeans Clustering:

Implement the standard KMeans clustering algorithm, using the given notion of distance (as defined in Task A), to obtain K=8 clusters of documents. Initialize the cluster centers randomly. Note: Do NOT use any ML library for this part.

Print the clusters into a file named ‘​kmeans.txt’​ in the same format as in Part B.

D. Attribute Reduction by Principal Component Analysis: [5 points]

Reduce the number of attributes of the dataset to 100 by using PCA. ​You can use the implementation of PCA from ​scikit-learn​(or from any equivalent library in other programming languages).

Use this reduced dataset and again obtain 8 clusters using your implementations of Agglomerative Clustering and KMeans Clustering. Print the clusters into files ‘agglomerative_reduced.txt’​ and ‘​kmeans_reduced.txt’​ respectively, in the same format as specified in part B.

</div>
</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="section">
<div class="layoutArea">
<div class="column">
E. Evaluation of the clusters:

Implement ​Normalized Mutual Information​(NMI) by writing a function that reads the dataset for the class labels, and one of the cluster files and prints the NMI score. Calculate this score for all the 4 sets of clusters you obtained from Tasks B, C and D; and include them in your ​README file. ​Note: Do NOT use any ML library for this part.

&nbsp;

</div>
</div>
</div>
</div>
