# 🚀 Throughput in System Design

**Throughput** ka matlab hota hai —  
> “Kitna data (ya requests) system ek certain time period mein process kar sakta hai.”

Ye system ki **speed aur efficiency** ko measure karta hai.  
Aap ise **“rate of work done”** bhi keh sakte ho.

---

## 🧠 Simple Definition

**Throughput = Successful requests per second*

Matlab ek second mein system kitni requests successfully process kar raha hai.

---

## 💬 Example

Agar tumhara web server 1 second mein 100 user requests handle karta hai,  
to system ka throughput hai:

> **100 requests/second**

Agar tumhara system har second 10MB data transfer karta hai,  
to throughput = **10 MB/sec**

---

## ⚙️ Formula

Throughput = (Total number of requests processed successfully) / (Total time taken)

---

## 📊 Example Scenarios

| System | Example Task | Throughput |
|---------|----------------|------------|
| Web Server | 1000 requests in 10 sec | 100 req/sec |
| Database | 500 queries in 5 sec | 100 queries/sec |
| Network | 100 MB data in 10 sec | 10 MB/sec |

---

## 🧩 Throughput vs Latency

| Metric | Meaning | Example |
|--------|----------|---------|
| **Latency** | Ek request complete hone ka delay | 200ms per request |
| **Throughput** | Kitni requests per second process hui | 100 req/sec |

🧠 **Analogy:**  

- Latency = ek car ko ek point se dusre tak jaane mein kitna time lagta hai.  
- Throughput = 1 minute mein kitni cars guzri road se.

---

## 💥 Factors Affecting Throughput

1. **CPU Performance** — Slow CPU → slow processing → low throughput.  
2. **Memory (RAM)** — Kam memory hone par caching aur parallel request handling slow hoti hai.  
3. **Disk I/O** — Slow SSD/HDD data read/write bottleneck create karta hai.  
4. **Network Bandwidth** — Kam bandwidth hone par data transfer slow hota hai.  
5. **Database Bottleneck** — Slow queries throughput ko drastically reduce karti hain.  
6. **Concurrency Limit** — Simultaneous threads/processes kam hone par requests queue hoti hain.

---

## ⚡ How to Improve Throughput

### 🔹 1. Caching

- Frequently used data cache me store karo (Redis, Memcached).
- Har bar DB query nahi karni padti → faster response → higher throughput.

### 🔹 2. Load Balancing

- Multiple servers use karo, jahan request evenly distribute ho.
- Example: 1 server → 100 req/sec, 10 servers → 1000 req/sec.

### 🔹 3. Database Optimization

- Proper indexing use karo.  
- Avoid unnecessary joins.  
- Use read replicas for read-heavy systems.

### 🔹 4. Asynchronous Processing

- Background jobs (queues) use karo jaise RabbitMQ, Kafka.  
- Long tasks async kar do → frontend request fast return kare.

### 🔹 5. Horizontal Scaling

- Zyada servers/machines add karo instead of upgrading ek hi server.

### 🔹 6. Compression

- Network data compress karke bhejo (gzip, brotli).  
- Less data → fast transfer → higher throughput.

### 🔹 7. Optimize Code Logic

- Unnecessary loops, heavy computations reduce karo.  
- Micro-optimizations (batch processing) use karo.

### 🔹 8. CDN (Content Delivery Network)

- Static files (images, CSS, JS) geographically closer servers se serve karo.  
- Network distance kam hone se throughput badhta hai.

---

## 🌍 Example: YouTube Throughput

| Component | Function | Optimization for High Throughput |
|------------|------------|--------------------------------|
| CDN | Serve videos | Geo-distributed servers |
| Encoder | Process video | Parallel encoding pipelines |
| Database | Store metadata | Sharding + caching |
| API | Handle users | Load balanced microservices |

---

## 🧮 Real-Life Analogy

Socho tumhara restaurant hai 🍔  

- **Latency** = Ek customer ko order milne mein lagne wala time  
- **Throughput** = 1 minute mein tum kitne orders serve kar rahe ho  

Agar tum extra chefs, faster kitchen tools aur pre-prepared ingredients lagao —  
to **throughput badh jata hai**!

---

## ✅ Summary Table

| Concept | Description |
|----------|--------------|
| **Throughput** | Number of requests processed per second |
| **Latency** | Time taken per request |
| **Goal** | Increase processed requests without compromising response time |
| **Improvement Techniques** | Caching, Load Balancing, Async Processing, Scaling |

---

## 🎯 Key Takeaway

> “High throughput means your system can handle more users efficiently,  
> without slowing down or crashing — it’s the true test of scalability.”
