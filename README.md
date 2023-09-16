# Matrix Multiplication with OpenMP

## Code Explanation

This program performs the following steps:

1. **Command-Line Arguments**: It accepts two command-line arguments - `matrix_size` and `num_threads`. These arguments determine the size of the matrices and the number of threads to use for parallel execution.

2. **Memory Allocation**: Dynamic memory allocation is used to create three matrices `A`, `B`, and `C`. These matrices will hold the input matrices and the result of matrix multiplication.

3. **Initialization**: Matrices `A` and `B` are initialized with the value 2, while matrix `C` is initialized with zeros.

4. **Parallel Matrix Multiplication**: The core matrix multiplication operation is parallelized using OpenMP. The `#pragma omp parallel for` directive splits the work among multiple threads. Each thread calculates a portion of the result matrix `C`.

5. **Timing**: The program measures the elapsed time for the matrix multiplication using the `gettimeofday` function. This provides a measure of the program's performance.

6. **Memory Deallocation**: After the matrix multiplication is complete, memory is deallocated to prevent memory leaks.

## How to Compile and Run

To compile the program, open a terminal and navigate to the directory containing the code. Use the following command:

```bash
gcc -o matrix_multiplication matrix_multiplication.c -fopenmp
```

This command compiles the code with OpenMP support and generates an executable named matrix_multiplication.

To run the program, use the following command:
```bash
./matrix_multiplication <matrix_size> <num_threads>
```

For finding nth power of the matrix:
```bash
./matrix_multiplication <matrix_size> <exponent> <num_threads>
```

Replace <matrix_size> with the desired size of the matrices and <num_threads> with the number of threads you want to use for parallel execution.
```bash
./matrix_multiplication 512 2
```

For nth power:
Replace <matrix_size> with the desired size of the matrices and <num_threads> with the number of threads you want to use for parallel execution.
```bash
./matrix_multiplication 512 2 4
```

This will perform matrix multiplication with matrices of size 1000x1000 using 4 threads.

## Output

The program will display the size of the matrices, the number of threads used, and the elapsed time for matrix multiplication.

Graph for the same are as below:

1. **OMM ( Threads vs Elapsed Time )** :

     ![image](https://github.com/Yasaswi-Vanarasi/SE23MAID016_1/assets/87477849/214d0bbe-35e7-4ec1-8885-55ffa655539d)
   
     ![image](https://github.com/Yasaswi-Vanarasi/SE23MAID016_1/assets/87477849/fd239863-8ad3-4060-90c6-238a7d9089a6)
   
     ![image](https://github.com/Yasaswi-Vanarasi/SE23MAID016_1/assets/87477849/8a838ed7-9a8a-4719-8aaf-1caffe1cff31)




   
3. **Nth Power of Matrix with OMM ( Threads vs Elapsed Time )** :

     ![image](https://github.com/Yasaswi-Vanarasi/SE23MAID016_1/assets/87477849/98dce8a4-782b-4628-bb9e-a3a3ba0c5eca)

     ![image](https://github.com/Yasaswi-Vanarasi/SE23MAID016_1/assets/87477849/e0d600fe-cbec-4e18-a571-8718296d6156)

     ![image](https://github.com/Yasaswi-Vanarasi/SE23MAID016_1/assets/87477849/c708ca09-be25-4136-96fb-b4e1f6591494)


## Conclusion

This C program demonstrates how to use OpenMP to parallelize matrix multiplication, improving the performance of the computation. You can adjust the matrix size and the number of threads to observe the impact on execution time.




# Block Matrix Multiplication

```markdown
# Block Matrix Multiplication

Compile the program using a C compiler. For example:

gcc -o block_matrix_mult block_matrix_mult.c -fopenmp
```

Here, block_matrix_mult is the name of the executable.

To run the program, use the following command-line format:
```bash
./block_matrix_mult <matrix_size> <num_threads> <block_size>
```

For nth power of a matrix using BMM:
```bash
./block_matrix_mult <matrix_size> <exponent> <num_threads> <block_size>
```

<matrix_size>: The size of the square matrices (e.g., 100 for a 100x100 matrix).
<block_size>: The size of the square blocks (e.g., 10 for a 10x10 block).
For example, to multiply two 100x100 matrices using 10x10 blocks:

```bash
./block_matrix_mult 1024 6 4
```

For nth power:
```bash
./block_matrix_mult 1024 2 6 4
```

## Output
The program will display the size of the matrices, the block size, and the result of the multiplication.

1. **BMM ( Threads vs Elapsed Time )** :

   ![image](https://github.com/Yasaswi-Vanarasi/SE23MAID016_1/assets/87477849/5459377d-77e7-4b33-9bfa-df1969f7fdf5)
   
   ![image](https://github.com/Yasaswi-Vanarasi/SE23MAID016_1/assets/87477849/4aec8243-0a1d-47ed-9441-78a87dc07970)
   
   ![image](https://github.com/Yasaswi-Vanarasi/SE23MAID016_1/assets/87477849/d7496767-f977-4375-b98e-5cb59c7320ce)
   
   ![image](https://github.com/Yasaswi-Vanarasi/SE23MAID016_1/assets/87477849/341b8577-f877-4c5c-bfd3-d4e921df4ea0)
   
   ![image](https://github.com/Yasaswi-Vanarasi/SE23MAID016_1/assets/87477849/8b305baa-2817-4843-ac36-ef156e2c22d4)
   
   ![image](https://github.com/Yasaswi-Vanarasi/SE23MAID016_1/assets/87477849/6ce478c7-09d3-4714-83c5-4e4cd8b9bb74)
   
   ![image](https://github.com/Yasaswi-Vanarasi/SE23MAID016_1/assets/87477849/a6a6a1e0-94da-4acb-a059-b7a5870c1b9f)
   
   ![image](https://github.com/Yasaswi-Vanarasi/SE23MAID016_1/assets/87477849/e3ac55d7-ad17-4c69-b271-1d0415428e56)
   
   ![image](https://github.com/Yasaswi-Vanarasi/SE23MAID016_1/assets/87477849/84c3ace2-2eaa-453e-b40e-17a9c8f6f8d1)
   
   ![image](https://github.com/Yasaswi-Vanarasi/SE23MAID016_1/assets/87477849/fc206d4f-83a1-4fee-81b4-7d83b519ab3d)
   
   ![image](https://github.com/Yasaswi-Vanarasi/SE23MAID016_1/assets/87477849/09644dc4-e1f0-464f-8d44-419a84ca86cb)
   
   ![image](https://github.com/Yasaswi-Vanarasi/SE23MAID016_1/assets/87477849/d2120d5c-d4bf-45f7-a6f4-9afa64cb7408)
   
   ![image](https://github.com/Yasaswi-Vanarasi/SE23MAID016_1/assets/87477849/cfe4e6f7-5a91-45bc-b4e0-fd36c79da57f)
   
   ![image](https://github.com/Yasaswi-Vanarasi/SE23MAID016_1/assets/87477849/a2540238-624c-4c5f-9de3-f9dcde4314fb)
   
   ![image](https://github.com/Yasaswi-Vanarasi/SE23MAID016_1/assets/87477849/d518ff1b-3dd9-4e1f-841c-92df52c39be7)


   
3. **Nth Power of Matrix with BMM ( Threads vs Elapsed Time )** :

   ![image](https://github.com/Yasaswi-Vanarasi/SE23MAID016_1/assets/87477849/51ba9293-04b2-4606-859c-329242a5c7a0)


   ![image](https://github.com/Yasaswi-Vanarasi/SE23MAID016_1/assets/87477849/f901caa2-3df8-4c0f-93fe-e4053b3ce89e)



## Memory Management
The program dynamically allocates memory for matrices A, B, and C, as well as for the block buffers. It frees the allocated memory after the multiplication is complete to prevent memory leaks.

