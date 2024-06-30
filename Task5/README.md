# Task 5

Dengan memanfaatkan program pada progjar6 (https://github.com/rm77/progjar/tree/master/progjar6), 

* Implementasikan arsitektur load balancer dengan
    * Mode asynchronous
    * Mode server thread
* Buatlah perbandingan kinerja web server 
* Buatlah gambar dari arsitektur percobaan
* Untuk pengukuran kinerja, gunakan tool
wrk dengan jumlah request/koneksi 1000, dengan parameter concurrency 10,50,100,150,200

```bash
wrk -c 1000 -t {n} http://url
```

* Laporkan kinerja dalam hal
    * Failed requests, request per second, waiting
* *** untuk meningkatkan performa, hilangkan beberapa overhead seperti print/mencetak log seluruh isi direktori/folder


## Results

| Load Balancer | jumlah concurrency | success | Average Latency (ms) | Total Transfer (KB) | Requests/sec | Transfer/sec |
|---------------|--------------------|---------|----------------------|---------------------|--------------|--------------|
|   lb_async    |         10         |   237   |         57.6         |         34.15       |     23.47    |     3.38     |
|               |         50         |   164   |        103.32        |         23.54       |     16.24    |     2.33     |
|               |         100        |   319   |         88.17        |         45.92       |     31.55    |     4.54     |
|               |         150        |	 451   |	    103.46        |	        64.74	    |     44.95    |     6.45     |
|               |	      200	     |   170   |	     91.98	      |          24.4   	|     16.82	   |     2.41     |


| Load Balancer | jumlah concurrency | success | Average Latency (ms) | Total Transfer (KB) | Requests/sec | Transfer/sec |
|---------------|--------------------|---------|----------------------|---------------------|--------------|--------------|
|   lb_thread	|	      10	     |    14   |         7.37	      |          2.01	    |      1.39	   |   0.20408    |
|               |	      50	     |	  19   |         10.42	      |          2.73	    |      1.88	   |   0.27664    |
|               |	      100	     |	  9    |         16.27	      |          1.29	    |      0.89	   |   0.13099    |
|               |	      150	     |	  13   |         11.1	      |          1.87	    |      1.29	   |    0.1892    |
|               |	      200	     |	  10   |         20.55 	      |          1.44	    |        1	   |    0.1464    |