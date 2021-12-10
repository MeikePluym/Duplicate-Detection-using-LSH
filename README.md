# Duplicate-Detection-using-LSH
An LSH approach to reduce computation time of duplicate detection
(Collaboration between Meike Pluym and Joram de Vreede)

This project is an assignment for the Erasmus School of Economics on duplicate detection in webshop data using an LSH approach to reduce the number of comparisons needed to be made.

The code is structured as follows;
The data is uploaded and a bootstrap of around 63% of the data is taken for evaluation of the method. Then, all product titles are cleaned and preprocessed, such that model words can be extracted from them. Consequently, model words which resemble a model ID are added to the vector of model words again. Binary vectors are created from the vector of model words.
The next step is to use minhashing to create (smaller) signatures of the binary vectors for each product. These signatures are then used in the LSH algorithm to produce candidate pairs for comparison.
The last part of the program compares the candidate pairs to find the duplicates and calculates some performance measures.

In the program, we set the number of bands in the LSH algorithm (b). Furthermore, we manually have to set a lower bound for similarity (e) in the comparison of the products.
