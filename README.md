# 🧑‍🏫 Synchronization-Problem---TA-Student-Simulation  

## 📌 Overview  
This project is a **C implementation of the classic “Sleeping Teaching Assistant (TA) Problem”**, a well-known **synchronization problem** in Operating Systems.  
It demonstrates how **students request help from the TA** while ensuring correct **synchronization** using **POSIX threads (pthreads)** and **semaphores**.  

The system simulates the following:  
- 👨‍🏫 The TA helps students **one at a time**.  
- 😴 If there are **no students waiting**, the TA goes to sleep.  
- 🪑 Students can wait on a limited number of chairs.  
- 🚶‍♂️ If all chairs are full, new students leave without getting help.  
- 🔒 Synchronization with **mutexes & semaphores** avoids race conditions.  

---

## ⚙️ Features  
- ✅ Simulation of **TA–Student interaction**.  
- ✅ Uses **pthreads** for concurrency.  
- ✅ Uses **semaphores** for synchronization.  
- ✅ Models a real-world **producer–consumer problem**.  
- ✅ Includes informative **console output** to observe behavior.  

---
## 🗂️ Project Structure  

Synchronization-Problem---TA-Student-Simulation/
│── main.c # Source code with TA and student threads
│── README.md # Project documentation



---

## 🖥️ How It Works  
1. The **TA thread** waits for students:  
   - If no student is waiting → TA sleeps.  
   - If students are waiting → TA helps one student at a time.  

2. **Student threads**:  
   - Try to sit on a chair if available.  
   - Wake the TA if the TA is asleep.  
   - If all chairs are full → student leaves.  

---

## 🚀 Getting Started  

### 🔧 Requirements  
- GCC compiler  
- POSIX threads library (`pthread`)  
- Linux / Unix environment (recommended)  

### 📥 Compilation  
```bash
gcc main.c -o simulation -lpthread

▶️ Run
./simulation

📚 Concepts Demonstrated

🔹 Concurrency & Parallelism

🔹 Synchronization using Semaphores

🔹 Producer–Consumer Problem

🔹 Operating Systems Scheduling Concepts

🤝 Contributing

Pull requests are welcome! For major changes, please open an issue first to discuss what you would like to change.

📜 License

This project is licensed under the MIT License – feel free to use, modify, and share
