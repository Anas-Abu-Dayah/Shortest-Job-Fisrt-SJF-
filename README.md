# Shortest-Job-Fisrt-SJF-
# Start
# Step 1-> In function swap(int *a, int *b)
  #  Set temp = *a
   # Set *a = *b
   # Set *b = temp
# Step 2-> In function arrangeArrival(int num, int mat[][3])
   # Loop For i=0 and i<num and i++
      # Loop For j=0 and j<num-i-1 and j++
         # If mat[1][j] > mat[1][j+1] then,
            # For k=0 and k<5 and k++
            # Call function swap(mat[k][j], mat[k][j+1])
# Step 3-> In function completionTime(int num, int mat[][3])
   # Declare temp, val
   # Set mat[3][0] = mat[1][0] + mat[2][0]
   # Set mat[5][0] = mat[3][0] - mat[1][0]
   # Set mat[4][0] = mat[5][0] - mat[2][0]
    # Loop For i=1 and i<num and i++
      # Set temp = mat[3][i-1]
      # Set low = mat[2][i]
      # Loop For j=i and j<num and j++
        # If temp >= mat[1][j] && low >= mat[2][j] then,
         #   Set low = mat[2][j]
          #  Set val = j
           # Set mat[3][val] = temp + mat[2][val]
           # Set mat[5][val] = mat[3][val] - mat[1][val]
           # Set mat[4][val] = mat[5][val] - mat[2][val]
           # Loop For  k=0; k<6; k++
           # Call function swap(mat[k][val], mat[k][i])
# Step 4-> In function int main()
  # Declare and set num = 3, temp
  # Declare and set mat[6][3] = {1, 2, 3, 3, 6, 4, 2, 3, 4}
  # Print Process ID, Arrival Time, Burst Time
  # Loop For i=0 and i<num and i++
   #   Print the values of mat[0][i], mat[1][i], mat[2][i]
    # Call function arrangeArrival(num, mat)
     # Call function completionTime(num, mat)
     # Print Process ID, Arrival Time, Burst Time, Waiting Time, Turnaround Time
     # Loop For i=0 and i<num and i++  
     # Print the values of  mat[0][i], mat[1][i], mat[2][i], mat[4][i], mat[5][i]
# Stop
