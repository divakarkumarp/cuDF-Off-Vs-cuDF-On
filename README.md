## cuDF-Off Vs cuDF-On
cuDF-Off refers to running code using standard pandas without any GPU acceleration, while cuDF-On refers to running the same code using cuDF's pandas Accelerator Mode to take advantage of GPU acceleration.
## How It Works
![image](https://github.com/user-attachments/assets/113061c3-50d6-47c8-b15e-770a20e21cc5)
![image](https://github.com/user-attachments/assets/4fdeb144-beee-4ee4-af5d-4f57be05534a)
## Performance Comparison
NVIDIA has compared the performance of cuDF-Off vs cuDF-On using the DuckDB Database-like ops benchmark, which measures the ability to perform tasks like grouped summary statistics and table joins on big datasets. According to NVIDIA, cuDF-On (denoted as xdf in the benchmark results) outperforms other high-performance Python data manipulation tools, including cuDF-Off.
The key advantages of cuDF-On are:
* Faster execution times for data manipulation tasks by leveraging GPU acceleration
* Up to 150x speed-up compared to running the same pandas workflow on the CPU
## Ease of Use
One of the main benefits of cuDF-On is the ease of use and compatibility with existing pandas code:
* You only need to write one line of code to enable GPU support and then you can write standard pandas code
* cuDF automatically switches between GPU and CPU as needed, so you don't have to handle the switching manually
* cuDF-On maintains compatibility with third-party libraries that work with pandas
## Limitations
While cuDF-On provides significant performance benefits, there are some limitations to be aware of:
* cuDF only implements about 60% of the pandas API currently, so some less common operations may not be supported
* cuDF-On requires an NVIDIA GPU to be available for GPU acceleration
* The performance will vary depending on the specific hardware, dataset, and calculations being performed
