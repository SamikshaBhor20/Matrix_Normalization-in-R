# Matrix_Normalization-in-R

# Matrix_Normalization-in-R

#Here first we read the data and convert it into numeric matrix adn further it will be normalized by by min_max function.

#Read the file:-
data<-read.csv("cancer.csv")
data


#Convert it into numeric matrix
data_matrix<-as.matrix(data)
data_numeric<-select_if(data_matrix,is.numeric)
data_numeric


##define Min-Max normalization function
min_max_norm <- function(x) {
  (x - min(x)) / (max(x) - min(x))
}
