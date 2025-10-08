# 📄 Debian Installation Report for IoT, MQTT, Kafka Course

> Students must complete all sections of this form during Debian installation and submit it upon completion.

---

## 🔧 General Information

| Title                  | Value                                               |
| -----------------------| --------------------------------------------------- |
| Full Name              | Theelawee Pengchanthaworn |
| Student ID             | 6510301033 |
| Installation Date      | 11 Jan 2025 |


---

## 🖥️ Device Information

- 💻 **Device Model / Type**: VM
- 🧬 **Firmware Type**:  
  - [ ] UEFI  
  - [x] BIOS  
- 🏷️ **Installation Type**:  
  - [ ] Physical PC  
  - [x] Virtual Machine (VM)

---

## 🗂️ Custom Partitioning

| Partition | Size  | Filesystem | Mount Point      | Notes             |
| --------- | ----- | ---------- | ---------------- | ----------------- |
| `/boot`   | 512MB | ext4       | `/boot`          | For boot loader   |
| `swap`    | 1GB   | swap       | -                | Swap space        |
| `/`       | 19GB  | ext4       | `/`              | Root filesystem   |
| `udev`    | 1.9GB | tmpfs      | `/dev`           | Device filesystem |
| `tmpfs`   | 392MB | tmpfs      | `/run`           | Runtime data      |
| `tmpfs`   | 2.0GB | tmpfs      | `/dev/shm`       | Shared memory     |
| `tmpfs`   | 5.0MB | tmpfs      | `/run/lock`      | Lock files        |
| `tmpfs`   | 392MB | tmpfs      | `/run/user/1000` | User runtime dir  |

---

## 🌐 Network Configuration (Static IP)

| Title                   | Value                                               |
| ------------------------| --------------------------------------------------- |
| Network Interface Name  | ens18    |
| IP Address              | 172.30.15.42 |
| Netmask                 | 255.255.255.0 |
| Gateway                 | 172.30.15.254 |
| DNS                     | 8.8.8.8 |

---

## 🖧 Hostname

- 🖥️ **Hostname Set**: FDT6510301033

---

## 👤 User Account

- 👨‍💻 **Username Created**: u6510301033
- 🔐 **Is a Root Password Set?**:  1234
  - [X] Yes  
  - [ ] No

---

## ✅ Additional Problems Notes (if any)

> _____________________________________________________________________  
> _____________________________________________________________________  
> _____________________________________________________________________

