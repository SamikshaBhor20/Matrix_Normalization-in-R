# Matrix_Normalization-in-R

# Matrix_Normalization-in-R
#Set the directory path
setwd("E:/Samiksha/M.Sc_Bioinformatics/SEM_3/Cancer_Genomics/Cancer_genomics_practical")

#Read the .csv data file
data<-read.csv("cancer.csv")
data

data1<-read.csv("cancer.csv", row.names = 1)
data1

#Normalization...CPM matrix--always column wise...no need to define as a vector

mat = data1

for(i in 1:ncol(data1)){                                                                   
  mat[,i]=(data1[,i]/sum(data1[,i]))*1000000
}

mat





#Substitute method of matrix normalization
 #Or we can calculate the CPM/LOG2 matrix by apply function
   #Or we can calculate the CPM/LOG2 matrix by apply function
 
 
 apply(data1[1:5, ], 1, sum)...here 1=row and 2=column
 cpm = apply(data1, 2, function(x) (x/sum(x))*1000000)
                                                                                                                                                                                
