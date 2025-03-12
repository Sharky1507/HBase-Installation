# 🚀 HBase Installation Guide (Windows)

## ⚠️ Prerequisites
Ensure that **Hadoop is installed and working** before proceeding, as HBase depends on it.

## 📌 Installation Steps

### 1️⃣ Download HBase
- Download **HBase 1.4.9** from the official Apache archive:  
  🔗 [Apache HBase 1.4.9](https://archive.apache.org/dist/hbase/1.4.9/)  
- Select and download the **third file** (with `.gz` extension).  
  ⚠️ Other versions may not be compatible with Windows.

### 2️⃣ Extract the Files
- Extract the downloaded files to `C:\` (root directory), so the path becomes:
  ```
  C:\hbase-1.4.9
  ```

### 3️⃣ Set Up Environment Variables
#### 🔹 User Variables:
- Open **Edit System Environment Variables** (search in Start Menu).
- Under **User variables**, click **New** and add:
  - **Variable Name:** `HBASE_HOME`
  - **Variable Value:** `C:\hbase-1.4.9`

#### 🔹 System Variables:
- Find the **Path** variable under **System Variables**.
- Click **Edit**, then **New**, and add:
  ```
  C:\hbase-1.4.9\bin
  ```
- Click **OK** to save the settings.

### 4️⃣ Configure HBase
- Navigate to `C:\hbase-1.4.9\conf`
- Replace `hbase-site.xml` with the one from the provided repository.

### 5️⃣ Set JAVA_HOME in `hbase-env.cmd`
- Open `C:\hbase-1.4.9\conf\hbase-env.cmd`
- Locate the **JAVA_HOME** line and modify it:
  ```
  set JAVA_HOME=C:\Progra~1\Java\jdk1.8.0_202
  ```
  ⚠️ If Java is installed in a different location, update the path accordingly.
- Save the file.

### 6️⃣ Start Hadoop Services
- Open **Command Prompt as Administrator**.
- Start Hadoop services by running:
  ```
  start-all.cmd
  ```
- Ensure all services start without errors.

### 7️⃣ Start HBase
- In the same command prompt or a new one, navigate to:
  ```
  cd C:\hbase-1.4.9\bin
  ```
- Run HBase Master Server:
  ```
  start-hbase.cmd
  ```
- If HBase is running properly, there should be **no error messages**.

### 8️⃣ Verify Installation
- Check running processes:
  ```
  jps
  ```
- If you see `HMaster` in the output, **HBase is running successfully** 🎉

### 9️⃣ Open HBase Shell
- Start the HBase shell by typing:
  ```
  hbase shell
  ```
- Now you can work with HBase! 🚀

---
🎯 **You're all set!** Happy data handling with HBase! 🎉

