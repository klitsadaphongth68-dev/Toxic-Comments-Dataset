# Toxic-Comments-Dataset
## 1. วัตถุประสงค์ของโครงงาน (Project Objectives)

โครงงานนี้มีวัตถุประสงค์เพื่อศึกษา วิเคราะห์ และประมวลผลข้อมูลความคิดเห็นจำนวน **30,000 รายการ** โดยเน้นระดับความเป็นพิษ (`Toxicity_Score`) ประเภทความคิดเห็น ความยาวความคิดเห็น แหล่งที่มา (`Platform`) และหัวข้อ (`Topic`)

**วัตถุประสงค์เฉพาะ:**
1. **Data Acquisition:** นำเข้าและตรวจสอบชุดข้อมูล `toxic_comments_dataset.csv`
2. **Data Inspection & Cleaning:** ตรวจสอบ Missing Values, Duplicate, Data Type และค่าตัวเลขผิดปกติ
3. **Correlation Analysis:** ศึกษาความสัมพันธ์ระหว่าง `Toxicity_Score` กับ `Comment_Length` และ `Word_Count`
4. **Group Analysis:** เปรียบเทียบระดับความเป็นพิษตาม `Platform`, `Topic` และ `Toxicity_Label`
5. **Distribution & Outlier Analysis:** ตรวจสอบการกระจายตัวและ Outliers ของ `Toxicity_Score`
6. **Visualization & Insights:** นำเสนอผลด้วยกราฟและตารางสรุป

## 2. สมาชิกและการแบ่งหน้าที่

| ลำดับ | สมาชิก | หน้าที่หลัก |
|---:|---|---|
| 1 | ณัฐชนน กรุณา 68114540782 | Data Preparation + Data Analysis |
| 2 | กฤษ 68114540782| Data Visualization + Findings |

## 3. คำถามการวิจัย (Research Questions)

* **RQ1:** `Toxicity_Score` มีความสัมพันธ์กับ `Comment_Length` และ `Word_Count` หรือไม่?
* **RQ2:** ระดับความเป็นพิษแตกต่างกันตาม `Platform`, `Topic` และ `Toxicity_Label` หรือไม่?
* **RQ3:** การกระจายตัวของ `Toxicity_Score` เป็นอย่างไร และมี Outliers ตามเกณฑ์ IQR หรือไม่?
