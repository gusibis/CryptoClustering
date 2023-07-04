# CryptoClustering

<div>Instructions</div>
<br>
<div>Rename the Crypto_Clustering_starter_code.ipynb file as Crypto_Clustering.ipynb.</div>
<br>
<div>Load the crypto_market_data.csv into a DataFrame.</div>
<br>
<div>Get the summary statistics and plot the data to see what the data looks like before proceeding.</div>
<br>
<div>Prepare the Data</div>
<div>Use the StandardScaler() module from scikit-learn to normalize the data from the CSV file.</div>
<br>
<div>Create a DataFrame with the scaled data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.</div>
<br>
<h2>Find the Best Value for k Using the Original Scaled DataFrame</h2>
<h2>Optimize Clusters with Principal Component Analysis</h2>
<h2>Find the Best Value for k Using the PCA Data</h2>
<h2>Cluster Cryptocurrencies with K-means Using the PCA Data</h2>

<br>
<div>Jupiter notebook location is "./Starter_Code/Crypto_Clustering.ipynb"</div>
<br>
<div>CSV file location is "./Starter_Code/Resources/crypto_market_data.csv"</div>

<div>   
    <p>In this challenge, you’ll use your knowledge of Python and unsupervised learning to predict if cryptocurrencies are affected by 24-hour or 7-day price changes.</p>
    <h3>Before You Begin</h3>
    <ol>
        <li>
            <p>Create a new repository for this project called <code>CryptoClustering</code>. <strong>Do not add this homework to an existing repository</strong>.</p>
        </li>
        <li>
            <p>Clone the new repository to your computer.</p>
        </li>
        <li>
            <p>Push your changes to GitHub.</p>
        </li>
    </ol>


    <h3>Instructions</h3>
    <ol>
        <li>
            <p>Rename the <code>Crypto_Clustering_starter_code.ipynb</code> file as <code>Crypto_Clustering.ipynb</code>.</p>
        </li>
        <li>
            <p>Load the <code>crypto_market_data.csv</code> into a DataFrame.</p>
        </li>
        <li>
            <p>Get the summary statistics and plot the data to see what the data looks like before proceeding.</p>
        </li>
    </ol>
    <h4>Prepare the Data</h4>
    <ul>
        <li>
            <p>Use the <code>StandardScaler()</code> module from <code>scikit-learn</code> to normalize the data from the CSV file.</p>
        </li>
        <li>
            <p>Create a DataFrame with the scaled data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.</p>
            <ul>
                <li>
                    <p>The first five rows of the scaled DataFrame should appear as follows:</p>
                    <p><img src="https://static.bc-edx.com/data/dl-1-2/m19/lms/img/scaled_DataFrame.png" alt="The first five rows of the scaled DataFrame" tabindex="0" role="button" aria-label="The first five rows of the scaled DataFrame. Click to Enlarge."></p>
                </li>
            </ul>
        </li>
    </ul>
    <h4>Find the Best Value for k Using the Original Scaled DataFrame</h4>
    <p>Use the elbow method to find the best value for <code>k</code> using the following steps:</p>
    <ul>
        <li>Create a list with the number of k values from 1 to 11.</li>
        <li>Create an empty list to store the inertia values.</li>
        <li>Create a <code>for</code> loop to compute the inertia with each possible value of <code>k</code>.</li>
        <li>Create a dictionary with the data to plot the elbow curve.</li>
        <li>Plot a line chart with all the inertia values computed with the different values of <code>k</code> to visually identify the optimal value for <code>k</code>.</li>
        <li>Answer the following question in your notebook: What is the best value for <code>k</code>?</li>
    </ul>
    <h4>Cluster Cryptocurrencies with K-means Using the Original Scaled Data</h4>
    <p>Use the following steps to cluster the cryptocurrencies for the best value for <code>k</code> on the original scaled data:</p>
    <ul>
        <li>Initialize the K-means model with the best value for <code>k</code>.</li>
        <li>Fit the K-means model using the original scaled DataFrame.</li>
        <li>Predict the clusters to group the cryptocurrencies using the original scaled DataFrame.</li>
        <li>Create a copy of the original data and add a new column with the predicted clusters.</li>
        <li>Create a scatter plot using hvPlot as follows:
            <ul>
                <li>Set the x-axis as "PC1" and the y-axis as "PC2".</li>
                <li>Color the graph points with the labels found using K-means.</li>
                <li>Add the "coin_id" column in the <code>hover_cols</code> parameter to identify the cryptocurrency represented by each data point.</li>
            </ul>
        </li>
    </ul>
    <h4>Optimize Clusters with Principal Component Analysis</h4>
    <ul>
        <li>
            <p>Using the original scaled DataFrame, perform a PCA and reduce the features to three principal components.</p>
        </li>
        <li>
            <p>Retrieve the explained variance to determine how much information can be attributed to each principal component and then answer the following question in your notebook:</p>
            <ul>
                <li>What is the total explained variance of the three principal components?</li>
            </ul>
        </li>
        <li>
            <p>Create a new DataFrame with the PCA data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.</p>
        </li>
    </ul>
    <h4>Find the Best Value for k Using the PCA Data</h4>
    <p>Use the elbow method on the PCA data to find the best value for <code>k</code> using the following steps:</p>
    <ul>
        <li>Create a list with the number of k-values from 1 to 11.</li>
        <li>Create an empty list to store the inertia values.</li>
        <li>Create a <code>for</code> loop to compute the inertia with each possible value of <code>k</code>.</li>
        <li>Create a dictionary with the data to plot the Elbow curve.</li>
        <li>Plot a line chart with all the inertia values computed with the different values of <code>k</code> to visually identify the optimal value for <code>k</code>.</li>
        <li>Answer the following question in your notebook:
            <ul>
                <li>What is the best value for <code>k</code> when using the PCA data?</li>
                <li>Does it differ from the best k value found using the original data?</li>
            </ul>
        </li>
    </ul>
    <h4>Cluster Cryptocurrencies with K-means Using the PCA Data</h4>
    <p>Use the following steps to cluster the cryptocurrencies for the best value for <code>k</code> on the PCA data:</p>
    <ul>
        <li>Initialize the K-means model with the best value for <code>k</code>.</li>
        <li>Fit the K-means model using the PCA data.</li>
        <li>Predict the clusters to group the cryptocurrencies using the PCA data.</li>
        <li>Create a copy of the DataFrame with the PCA data and add a new column to store the predicted clusters.</li>
        <li>Create a scatter plot using hvPlot as follows:
            <ul>
                <li>Set the x-axis as "price_change_percentage_24h" and the y-axis as "price_change_percentage_7d".</li>
                <li>Color the graph points with the labels found using K-means.</li>
                <li>Add the "coin_id" column in the <code>hover_cols</code> parameter to identify the cryptocurrency represented by each data point.</li>
            </ul>
        </li>
        <li>Answer the following question:
            <ul>
                <li>What is the impact of using fewer features to cluster the data using K-Means?</li>
            </ul>
        </li>
    </ul>
 
    <h3>Requirements</h3>
    <h4>Find the Best Value for k by Using the Original Data (15 points)</h4>
    <p>To receive all points, you must:</p>
    <ul>
        <li>
            <p>Code the elbow method algorithm to find the best value for k. Use a range from 1 to 11. (5 points)</p>
        </li>
        <li>
            <p>To visually identify the optimal value for k, plot a line chart of all the inertia values computed with the different values of k. (5 points)</p>
        </li>
        <li>
            <p>Answer the following question: What’s the best value for k? (5 points)</p>
        </li>
    </ul>
    <h4>Cluster the Cryptocurrencies with K-Means by Using the Original Data (10 points)</h4>
    <p>To receive all points, you must:</p>
    <ul>
        <li>
            <p>Initialize the K-means model with four clusters by using the best value for k. (1 point)</p>
        </li>
        <li>
            <p>Fit the K-means model by using the original data. (1 point)</p>
        </li>
        <li>
            <p>Predict the clusters for grouping the cryptocurrencies by using the original data. Review the resulting array of cluster values. (3 points)</p>
        </li>
        <li>
            <p>Create a copy of the original data, and then add a new column of the predicted clusters. (1 point)</p>
        </li>
        <li>
            <p>Using hvPlot, create a scatter plot by setting <code>x="price_change_percentage_24h"</code> and <code>y="price_change_percentage_7d"</code>. Color the graph points with the labels that you found by using K-means. Then add the crypto name to the <code>hover_cols</code> parameter to identify the cryptocurrency that each data point represents. (4 points)</p>
        </li>
    </ul>
    <h4>Optimize the Clusters with Principal Component Analysis (10 points)</h4>
    <p>To receive all points, you must:</p>
    <ul>
        <li>
            <p>Create a PCA model instance, and set <code>n_components=3</code>. (1 point)</p>
        </li>
        <li>
            <p>Use the PCA model to reduce the features to three principal components. Then review the first five rows of the DataFrame. (2 points)</p>
        </li>
        <li>
            <p>Get the explained variance to determine how much information can be attributed to each principal component. (2 points)</p>
        </li>
        <li>
            <p>Answer the following question: What’s the total explained variance of the three principal components? (3 points)</p>
        </li>
        <li>
            <p>Create a new DataFrame with the PCA data. Be sure to set the <code>coin_id</code> index from the original DataFrame as the index for the new DataFrame. Review the resulting DataFrame. (2 points)</p>
        </li>
    </ul>
    <h4>Find the Best Value for k by Using the PCA Data (10 points)</h4>
    <p>To receive all points, you must:</p>
    <ul>
        <li>
            <p>Code the elbow method algorithm, and use the PCA data to find the best value for k. Use a range from 1 to 11. (2 points)</p>
        </li>
        <li>
            <p>To visually identify the optimal value for k, plot a line chart of all the inertia values computed with the different values of k. (5 points)</p>
        </li>
        <li>
            <p>Answer the following questions: What’s the best value for k when using the PCA data? Does it differ from the best value for k that you found by using the original data? (3 points)</p>
        </li>
    </ul>
    <h4>Cluster the Cryptocurrencies with K-means by Using the PCA Data (10 points)</h4>
    <p>To receive all points, you must:</p>
    <ul>
        <li>
            <p>Initialize the K-means model with four clusters by using the best value for k. (1 point)</p>
        </li>
        <li>
            <p>Fit the K-means model by using the PCA data. (1 point)</p>
        </li>
        <li>
            <p>Predict the clusters for grouping the cryptocurrencies by using the PCA data. Review the resulting array of cluster values. (3 points)</p>
        </li>
        <li>
            <p>Create a copy of the DataFrame with the PCA data, and then add a new column to store the predicted clusters. (1 point)</p>
        </li>
        <li>
            <p>Using hvPlot, create a scatter plot by setting <code>x="PC1"</code> and <code>y="PC2"</code>. Color the graph points with the labels that you found by using K-means. Then add the crypto name to the <code>hover_cols</code> parameter to identify the cryptocurrency that each data point represents. (4 points)</p>
        </li>
    </ul>
    <h4>Visualize and Compare the Results (15 points)</h4>
    <p>To receive all points, you must:</p>
    <ul>
        <li>
            <p>Create a composite plot by using hvPlot and the plus sign (<code>+</code>) operator to compare the elbow curve that you created from the original data with the one that you created from the PCA data. (5 points)</p>
        </li>
        <li>
            <p>Create a composite plot by using hvPlot and the plus (<code>+</code>) operator to compare the cryptocurrency clusters that resulted from using the original data with those that resulted from the PCA data. (5 points)</p>
        </li>
        <li>
            <p>Answer the following question: Based on visually analyzing the cluster analysis results, what’s the impact of using fewer features to cluster the data by using K-means? (5 points)</p>
        </li>
    </ul>
    <h4>Coding Conventions and Formatting (10 points)</h4>
    <p>To receive all points, you must:</p>
    <ul>
        <li>
            <p>Place imports at the top of the file, just after any module comments and docstrings, and before module globals and constants. (3 points)</p>
        </li>
        <li>
            <p>Name functions and variables with lowercase characters, with words separated by underscores. (2 points)</p>
        </li>
        <li>
            <p>Follow DRY (Don't Repeat Yourself) principles, creating maintainable and reusable code. (3 points)</p>
        </li>
        <li>
            <p>Use concise logic and creative engineering where possible. (2 points)</p>
        </li>
    </ul>
    <h4>Deployment and Submission (10 points)</h4>
    <p>To receive all points, you must:</p>
    <ul>
        <li>
            <p>Submit a link to a GitHub repository that’s cloned to your local machine and that contains your files. (4 points)</p>
        </li>
        <li>
            <p>Use the command line to add your files to the repository. (3 points)</p>
        </li>
        <li>
            <p>Include appropriate commit messages in your files. (3 points)</p>
        </li>
    </ul>
    <h4>Code Comments (10 points)</h4>
    <p>To receive all points, your code must:</p>
    <ul>
        <li>Be well commented with concise, relevant notes that other developers can understand. (10 points)</li>
    </ul>
</div>


  