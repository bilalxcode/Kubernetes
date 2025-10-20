# 🧠 Replication Controller,ReplicaSet,Deployment

## ⚙️ 1. Replication Controller (Legacy)
- Acts as a **manual autoscaler**  
- Can span **multiple nodes**  
- **Only manages pods** that it created  
- Considered **legacy**, replaced by **ReplicaSet**

---

## 🧩 2. ReplicaSet
- **Newer version** of Replication Controller  
- Can **manage existing pods** using **selectors** (match labels)  
- Supports **multiple ways to scale** (manual or autoscaling)  
- Commonly managed by **Deployments**
![image](https://github.com/piyushsachdeva/CKA-2024/assets/40286378/3e9792d4-1127-44b4-a6ec-cdc2a82219e3)

---

## 🚀 3. Deployment
- **Manages ReplicaSets** and ensures **seamless updates**  
- Uses **rolling updates** — users are **not impacted during updates**  
- Automatically **creates and manages ReplicaSets**
![image](https://github.com/piyushsachdeva/CKA-2024/assets/40286378/b888d272-c623-4a00-8381-45c25ce9d9c0)

---

### ✅ Summary
| Component | Purpose | Notes |
|------------|----------|-------|
| **Replication Controller** | Legacy scaling controller | Only manages its own pods |
| **ReplicaSet** | Modern pod controller | Uses selectors, supports scaling |
| **Deployment** | Manages ReplicaSets | Handles rolling updates and versioning |

---

📘 **Key Takeaway:**  
Use **Deployments** for managing application lifecycle — they handle **ReplicaSets** automatically and provide **safe, zero-downtime updates**.