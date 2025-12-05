# Lab 7 – Backup & Recovery Basics  
**Windows Server 2022 | DC01**

This lab demonstrates how to install Windows Server Backup, configure full and incremental backups, simulate data loss, and perform file recovery on DC01.

---

## 📌 **Objectives**
- Install and enable **Windows Server Backup** feature  
- Create a **dedicated virtual disk** for backups  
- Run a **Full Server backup**  
- Create test data and perform an **incremental backup**  
- Simulate data loss  
- Use the **Recovery Wizard** to restore deleted files  
- Validate recovery results

---

## 📂 **Screenshots**
All screenshots are located in the `screenshots/` folder:

Lab07-01_server-backup-feature-added.png
Lab07-02_installation-success.png
Lab07-03_backup-schedule-wizard.png
Lab07-04_select-items-to-backup.png
Lab07-05_backup-schedule-summary.png
Lab07-06_full-backup-start.png
Lab07-07_full-backup-completed.png
Lab07-08_test-folder-created.png
Lab07-09_test-files-created.png
Lab07-10_incremental-backup-start.png
Lab07-11_incremental-backup-completed.png
Lab07-12_files-deleted.png
Lab07-13_folder-missing.png
Lab07-14_select-restore-point.png
Lab07-15_recovery-wizard.png
Lab07-16_recovery-success.png

markdown
Copy code

---

## 🛠️ **Part 1 — Install Windows Server Backup**

1. Open **Server Manager → Add Roles and Features**  
2. Under **Features**, check:  
   - ✔ Windows Server Backup  
3. Complete the installation  

📸 *See:* `Lab07-01_server-backup-feature-added.png`  
📸 *See:* `Lab07-02_installation-success.png`

---

## 💽 **Part 2 — Add a Backup Disk (20 GB)**

1. Shut down the VM  
2. Add a new **VirtIO drive** (20 GB)  
3. Boot the server  
4. Open **Disk Management**  
5. Bring the disk **Online**  
6. Leave as **Unallocated** (Windows Backup will format it)

---

## 🔄 **Part 3 — Run a Full Backup (Backup Once)**

1. Open **Windows Server Backup**  
2. Select **Backup Once…**  
3. Choose **Full Server**  
4. Select the new 20 GB disk  
5. Choose **VSS Copy Backup**  
6. Start the backup

📸 *See:*  
`Lab07-03_backup-schedule-wizard.png`  
`Lab07-04_select-items-to-backup.png`  
`Lab07-05_backup-schedule-summary.png`  
`Lab07-06_full-backup-start.png`  
`Lab07-07_full-backup-completed.png`

---

## 📁 **Part 4 — Create Test Data**

1. Navigate to **C:\**  
2. Create a folder named **TestData**  
3. Add two files:  
   - `report1.txt`  
   - `report2.txt`

📸 *See:*  
`Lab07-08_test-folder-created.png`  
`Lab07-09_test-files-created.png`

---

## 🔄 **Part 5 — Run an Incremental Backup**

1. Open **Backup Once…** again  
2. Select **Full Server**  
3. Use same backup disk  
4. Perform the incremental backup

📸 *See:*  
`Lab07-10_incremental-backup-start.png`  
`Lab07-11_incremental-backup-completed.png`

---

## 🗑️ **Part 6 — Simulate Data Loss**

1. Delete the **TestData** folder completely  
2. Refresh File Explorer to confirm it is missing  

📸 *See:*  
`Lab07-12_files-deleted.png`  
`Lab07-13_folder-missing.png`

---

## 🔁 **Part 7 — Recover Deleted Files**

1. Open **Windows Server Backup**  
2. Click **Recover…**  
3. Choose **This server**  
4. Select the appropriate backup date  
5. Choose **Files and Folders**  
6. Select **TestData** for recovery  
7. Recover to **Original Location**  
8. Complete the wizard  

📸 *See:*  
`Lab07-14_select-restore-point.png`  
`Lab07-15_recovery-wizard.png`  
`Lab07-16_recovery-success.png`

---

## ✅ **Part 8 — Verification**

After recovery:

- Navigate to **C:\TestData**
- Confirm **report1.txt** and **report2.txt** are restored

---

## 🧠 **What I Learned**

- How Windows Server Backup handles **full** vs **incremental** backups  
- How VSS (Volume Shadow Copy Service) supports snapshotting  
- How to configure and use dedicated backup disks  
- How to use the **Recovery Wizard** for granular file restoration  
- How to validate backup health and recovery results  

---

## 📘 **Tools & Technologies Used**
- Windows Server 2022  
- Windows Server Backup feature  
- VSS Full / Copy backups  
- Virtual disks (VirtIO)  
- File Explorer  
- Disk Management  

---