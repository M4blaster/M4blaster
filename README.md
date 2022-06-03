- 👋 Hi, I’m @M4blaster
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...

- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
M4blaster/M4blaster is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
       MEAN
# create a vector.
x <- c(54,38,12,74,36,71,24,64,95)
#Find Mean .
result.mean <- mean(x)           
print(result.mean)

**********************
MEdian
# create the vector
x <- c(54,38,12,74,36,71,24,64,95)
#Find Median.
result.mean <- median(x)           
print(median.result)



***********************
MODE
# Create the function. 
getmode <- function(v) { 
 uniqv <- unique(v) 
 uniqv[which.max(tabulate(match(v,uniqv)))] 
} 
# Create the vector with numbers. 
v <- c(2,1,2,3,1,2,3,4,1,5,5,3,2,3) 
# Calculate the mode using the user function. 
result <- getmode(v) 
print(result) 
# Create the vector with characters. 
charv <- c("o","it","the","it","it") 
# Calculate the mode using the user function. 
result <- getmode(charv) 
print(result)
