# homework1
#sampling with replacement using complements

#find the amount of times out of 1e6 that atleast 2 out of 36 people share #the same birthday

##establish variables
i = 1
j = 0
##create loop to run the code
while (i <= 1000000) {
  ##establish the sample
  result = sample (1:365, replace = TRUE, 36)
  ##if there are atleast 2 of the same number, count that
  if (length(unique(result)) < 36) {
    j = j + 1
  }
  i = i + 1
}
##print the final sum of all the times there were 2 or more of the same number
print(j)
