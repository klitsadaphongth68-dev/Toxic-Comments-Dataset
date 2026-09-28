# Toxic-Comments-Dataset

## 1. วัตถุประสงค์ของโครงงาน (Project Objectives)

โครงงานนี้มีวัตถุประสงค์เพื่อศึกษา วิเคราะห์ และสร้างแบบจำลองจากข้อมูลความคิดเห็นจำนวน 30,000 รายการ โดยเน้นการวิเคราะห์ระดับความเป็นพิษของความคิดเห็น (`Toxicity_Score`) ประเภทหรือระดับความเป็นพิษ (`Toxicity_Label`) รวมถึงปัจจัยที่เกี่ยวข้อง เช่น ความยาวความคิดเห็น (`Comment_Length`), จำนวนคำ (`Word_Count`), แหล่งที่มาของความคิดเห็น (`Platform`), หัวข้อ (`Topic`) และระดับความสำคัญในการตรวจสอบ (`Moderation_Priority`)

วัตถุประสงค์เฉพาะ:

1. **Data Understanding:** ตรวจสอบโครงสร้างข้อมูล ชนิดข้อมูล Missing Values, Duplicate และลักษณะของตัวแปรใน Dataset
2. **Data Visualization:** วิเคราะห์การกระจายตัว ความสัมพันธ์ และรูปแบบของข้อมูลด้วยกราฟ Univariate, Bivariate, Target-focused และ Multivariate Visualization
3. **Deep EDA:** วิเคราะห์ Outliers, IQR, Skewness, Kurtosis, QQ Plot, Normality และ Multicollinearity เพื่อทำความเข้าใจลักษณะของข้อมูลและกำหนดแนวทาง Preprocessing
4. **Hypothesis Testing:** ทดสอบความสัมพันธ์ระหว่างตัวแปรเชิงหมวดหมู่และระดับความเป็นพิษ รวมถึงทดสอบความแตกต่างของระดับความเป็นพิษระหว่างกลุ่ม
5. **Problem Framing:** กำหนดปัญหาเป็น **Multiclass Classification** โดยใช้ `Toxicity_Label` เป็น Target และกำหนด **Macro F1** เป็น Metric หลักในการประเมินโมเดล
6. **Model Selection:** เปรียบเทียบโมเดล Classification หลายวิธีด้วย **5-Fold Stratified Cross-Validation** และประเมิน Final Model บน Test Set
7. **Model Evaluation:** วิเคราะห์ผลการทำนายด้วย Accuracy, Macro F1, Macro AUC, Classification Report และ Confusion Matrix

## 2. สมาชิกและการแบ่งหน้าที่

| ลำดับ | สมาชิก | หน้าที่หลัก |
|---:|---|---|
| 1 | ณัฐชนน กรุณา 68114540782 | Data Preparation + Data Analysis |
| 2 | กฤษฎาพงษ์ ทิณพัฒน์ 68114540054| Data Visualization + Findings |

## 2. คำถามการวิจัย (Research Questions)

- **RQ1:** `Toxicity_Score` มีความสัมพันธ์กับ `Comment_Length` และ `Word_Count` หรือไม่?

- **RQ2:** `Toxicity_Label` มีความสัมพันธ์กับ `Platform` และ `Topic` หรือไม่?

- **RQ3:** การกระจายตัวของ `Toxicity_Score` เป็นอย่างไร และมี Outliers ตามเกณฑ์ IQR หรือไม่?

- **RQ4:** ปัจจัยจากข้อมูลความคิดเห็น เช่น `Comment_Length`, `Word_Count`, `Platform`, `Topic` และ `Moderation_Priority` สามารถใช้จำแนก `Toxicity_Label` ซึ่งมี 5 classes ได้ดีเพียงใด?

- **RQ5:** โมเดล Classification แต่ละวิธีมีประสิทธิภาพแตกต่างกันอย่างไรเมื่อเปรียบเทียบด้วย 5-Fold Stratified Cross-Validation และ Macro F1?
