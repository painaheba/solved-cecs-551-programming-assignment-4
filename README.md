Download Link: https://assignmentchef.com/product/solved-cecs-551-programming-assignment-4
<br>



<strong> </strong>

Submit a paper containing the solutons to each of the exercises found below. The paper should be divided into two sections: Solutions, and Appendix. Each solution should be clearly presented and accompanied by narrative when necessary. Source code should <em>not </em>be included in the Solutions section unless explicitly requested. However, all supporting source code should be included in the appendix. Both Solutions and Appendix should be divided into sections, titled EXERCISE 1, EXERCISE 2, etc.. <strong>Important: </strong>credit for an exercise will not be awarded if there is insufficient supporting source code in the appendix.

<strong>Exercises</strong>

<ol>

 <li>Review and download the abalone data set at</li>

</ol>

http://archive.ics.uci.edu/ml/datasets/Abalone?pagewanted=all

Use the e1071 library’s svm function on the data set with at least 20 different combinations of polynomial degree and <em>C </em>cost. For each combination perform the following: i) 10-fold cross validation, and ii) training accuracy from training over the entire data set. Make a table showing the results. The table should order the combinations by increasing complexity. Note: assume (<em>d</em><sub>1</sub><em>,C</em><sub>1</sub>) induces a more complex model than (<em>d</em><sub>2</sub><em>,C</em><sub>2</sub>) iff either <em>d</em><sub>1 </sub><em>&gt; d</em><sub>2</sub>, or <em>C</em><sub>1 </sub><em>&lt; C</em><sub>2</sub>. Highlight the combination that resulted in highest average CV accuracy. Note: the 20 different combinations for <em>d </em>and <em>C </em>should provide a good variation of svm model possibilities. For the best classifier in the table, provide the average distance of the predicted class from the true class. Provide a histogram that shows the frequency of how often a predication is <em>m </em>rings away from the true number of rings, where <em>m </em>= 0<em>,</em>1<em>,</em>2<em>,…,</em>29.

1

<ol start="2">

 <li>Consider the following alternative method for classifying the ring count of an abalone. Thismethod uses the following nine binary classifiers: <em>f</em><sub>≤9 </sub>vs <sub>≥10</sub>, <em>f</em><sub>≤7 </sub>vs <sub>8−9</sub>, <em>f</em><sub>≤5 </sub>vs <sub>6−7</sub>, <em>f</em><sub>8 </sub>vs <sub>9</sub>, <em>f</em><sub>6 </sub>vs 7, <em>f</em><sub>10</sub>−<sub>11 </sub>vs ≥<sub>12</sub>, <em>f</em><sub>12</sub>−<sub>13 </sub>vs ≥<sub>14</sub>, <em>f</em><sub>10 </sub>vs 11, <em>f</em><sub>12 </sub>vs 13. For example <em>f</em>≤<sub>7 </sub>vs 8−<sub>9 </sub>classifies an abalone data point as either having 7 or fewer rings, or having either 8 or 9 rings. Thus, the training set for this classifier consists of all training points with 9 or fewer rings. As another example <em>f</em><sub>8 </sub>vs <sub>9 </sub>classifies an abalone data point as either having 8 rings or 9 rings. Thus, the training set for this classifier consists of all training points with 8 or 9 or fewer rings. These binary classifiers are used to form a classification algorithm that behaves in a manner similar to binary search. For example, on input <em><span style="text-decoration: line-through;">x</span></em>, we first evaluate <em>f</em><sub>≤9 </sub>vs <sub>≥10</sub>(<em><span style="text-decoration: line-through;">x</span></em>). Suppose the output is +1 (i.e. <em><span style="text-decoration: line-through;">x </span></em>is classified as having at least 10 rings). Next we evaluate <em>f</em><sub>10−11 </sub>vs <sub>≥12</sub>(<em><span style="text-decoration: line-through;">x</span></em>). Suppose the output is −1 (i.e. . <em><span style="text-decoration: line-through;">x </span></em>is classified as having 10 or 11 rings). Finally, the algorithm evaluates <em>f</em><sub>10 </sub>vs <sub>11</sub>(<em><span style="text-decoration: line-through;">x</span></em>) and returns either 10 or 11 as the final ring classification. In the case where <em><span style="text-decoration: line-through;">x </span></em>is classified as having 5 or fewer rings, then the algorithm outputs 5. Similarly, in the case where <em><span style="text-decoration: line-through;">x </span></em>is classified as having 14 or more rings, then the algorithm outputs 14.</li>

</ol>

For each of the nine classifiers, use a method similar to that used in Exercise 1 for finding a best svm model for the classifier. Provide a table having nine rows, where each row reports on the best classifier found for each of the nine different classifiers. Each row should include i) a description of the two classes (e.g. “10 vs 11”), ii) size of the training set, iii) degree value of best learning-parameter (BLP) combination, iv) <em>C </em>value of BLP combination v) the average CV accuracy for the BLP combination, and vi) the training accuracy of the final model constructed with the best learning parameters.

<ol start="3">

 <li>Implement the binary-search learning algorithm described in the previous exercise, and applyit to the entire abalone data set. Report on the training accuracy and the average distance of the predicted class from the true class. Provide a histogram that shows the frequency of how often a predication is <em>m </em>rings away from the true number of rings, where <em>m </em>= 0<em>,</em>1<em>,</em>2<em>,…,</em></li>

 <li>Use the two-dimensional data in file Exercise-4.csv to build a data frame df. Use R’s plot function to visualize the data. Verify that the relationship between <em>x </em>and <em>y </em>appears to be quadratic. Use the e1071 library’s svm function (with the following options kernel = ‘‘polynomial’’, degree = 2, type = ‘‘eps-regression’’</li>

</ol>

held constant) on the data set with at least 20 different combinations of <em> </em>and <em>C </em>cost. For each combination perform the following: i) 10-fold cross validation of mean squared error (mse), and ii) mse over the entire data set. Make a table showing the results. The table should order the combinations by increasing complexity. Note: assume () induces a more complex model than () iff either , or <em>C</em><sub>1 </sub><em>&lt; C</em><sub>2</sub>. Highlight the combination that resulted in highest average CV mse. Again, the 20 different combinations for <em> </em>and <em>C </em>should provide a good variation of svm model possibilities.

<ol start="5">

 <li>Provide a graph that shows the plotted data points against the curve provided by the best svmfrom the previous exercise. Plot the svm model using 1,000 data points equally spaced between 0 to 10. Make sure the plotted data points and plotted model points are clearly distinguishable.</li>

 <li>Try different combinations of <em>d</em>, <em>C</em>, and to find a good support-vector regression machine for the abalone data set. Report on the average distance of the predicted class from the true class. Provide a histogram that shows the frequency of how often a predication is <em>m </em>rings away from the true number of rings, where <em>m </em>= 0<em>,</em>1<em>,</em>2<em>,…,</em></li>

</ol>


