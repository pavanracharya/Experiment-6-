# **CURRENT MIRROR DESIGN AND ANALYSIS**

## **Contents**
1. Introduction to Current Mirror  
2. Applications of Current Mirror  
3. Advantages and Disadvantages  
4. Design and Analysis
    - Circuit 1: *180nm technology*
        - Case 1: *Mirror Ratio 1:1*
          - DC Analysis  
          - AC Analysis  
          - Transient Analysis   
        - Case 2: *Mirror Ratio 1:2*
          - DC Analysis  
          - AC Analysis  
          - Transient Analysis
            
    - Circuit 2: *500nm technology*
        - DC Analysis  
        - AC Analysis  
        - Transient Analysis   

    - Circuit 3: *1um technology*
        - DC Analysis  
        - AC Analysis  
        - Transient Analysis   
      
5. Bonus Question
   
   -Circuit 1: *1:3 ratio*
      - DC Analysis  
      - AC Analysis
      - Transient Analysis
   
   -Circuit 2: *2:1 ratio*
      - DC Analysis  
      - AC Analysis
      - Transient Analysis
6. Result
7. Inference
   
## **1. Introduction to Current Mirror**

### **What is a Current Mirror?**
A **Current Mirror** is an analog circuit that replicates (mirrors) a reference current (**Iref**) to produce a stable output current. It is widely used in integrated circuits (ICs) for biasing and active loads. The circuit typically consists of two or more transistors with matched characteristics to ensure accurate current replication. **To generate \( V_b \) (bias voltage) insensitive to Process, Voltage, and Temperature (PVT) variations, we introduce \( I_{ref} \) (The Golden Reference Current). Another name for this circuit is the Bandgap Reference Circuit**, which provides a temperature-stable voltage. The performance of a current mirror depends on the matching of the transistors and the precision of the reference current.

### **Principle of Operation**
The basic current mirror consists of **two matched MOSFETs** or **BJTs**. One transistor sets the reference current (*I\(_{ref}\)*) while the other mirrors this current. The mirrored current depends on the **transistor dimensions (W/L ratio)** and **process parameters**.

## **2. Applications of Current Mirror**
- **Biasing Circuits**  
- **Current Sources**  
- **Differential Amplifiers**  
- **Cascode Amplifiers**  

## **3. Advantages and Disadvantages**

### **Advantages:**
- *Simple and easy to design.*  
- *Requires minimal transistor count.*  

### **Disadvantages:**
- *Limited output impedance.*  
- *Reduced accuracy due to channel-length modulation.*  

## **4. Design and Analysis**
### **Circuit 1**
### **case 1: Mirror Ratio 1:1**

*Given Parameters:*
- \( 180nm technology )  
- \( Power = 1mW )  
- \( I_{ref} = 0.277 \uA \)  
- \( V_{DD} = 1.8V \)  

**MOSFET Drain Current Equation:**

\[
I_D = ![image](https://github.com/user-attachments/assets/6abe4392-2075-4bda-8411-9b0129d469c3)
\]

| *Parameters*  | *M1*   | *M2*   | *M3*       |
| ------------- | ------ | ------ | ---------- |
| **Model**     | CMOSP  | CMOSP  | CMOSN      |
| **Length (m)**| 180n   | 180n   | 180n       |
| **Width (m)** | 100u    | 100u    |28.2um   |
| **Current (A)**| 0.277m  | 0.277m  | 0.277m      |

**DC analysis**

![1_1 op](https://github.com/user-attachments/assets/251d3475-68d3-4025-b369-75a9d2d904c2)


**Transient Analysis**

![Screenshot 2025-03-24 145702](https://github.com/user-attachments/assets/63ae186d-0bc0-485b-bffc-0aaee6dca3e2)



**AC analysis**

![Screenshot 2025-03-24 145824](https://github.com/user-attachments/assets/527c0f47-d2d3-442f-b167-cf9dcacfe52f)

 
---

### **case 2: Mirror Ratio 1:2**

*Given Parameters:*  
- \( L = 180nm \)

| *Parameters*  | *M1*   | *M2*   | *M3*       |
| ------------- | ------ | ------ | ---------- |
| **Model**     | CMOSP  | CMOSP  | CMOSN      |
| **Length (m)**| 180n   | 180n   | 180n       |
| **Width (m)** | 100u    | 200u    | 56.9u   |
| **Current (A)**| 0.277m  | 0.554m  | 0.554m      |

**DC analysis**
![Screenshot 2025-03-24 071450](https://github.com/user-attachments/assets/2ad70782-ddf3-4fab-9d47-f684f58a5ba6)

**Transient Analysis**
![Screenshot 2025-03-24 071633](https://github.com/user-attachments/assets/ec5ff85a-47d8-460b-965a-29c07ef2d3b7)

**AC analysis**
![Screenshot 2025-03-24 072120](https://github.com/user-attachments/assets/76215df4-a9ee-4a7d-9e83-f7d643cbce64)

---

### **Circuit 3**
## **Using 1um technology**

| *Parameters*  | *M1*   | *M2*   | *M3*       |
| ------------- | ------ | ------ | ---------- |
| **Model**     | CMOSP  | CMOSP  | CMOSN      |
| **Length (m)**| 1u   | 1u  | 1u      |
| **Width (m)** | 100u    | 100u    | 86.5u  |
| **Current (A)**| 0.2777m| 0.2777m| 0.2777m    |

**DC analysis**
![Screenshot 2025-03-24 151756](https://github.com/user-attachments/assets/f9f83374-3bb4-4bae-8e16-705ac15a240e)

**Transient Analysis**
![Screenshot 2025-03-24 152016](https://github.com/user-attachments/assets/b4a5a514-02d9-4915-8669-bc5ee2dc4d14)

**AC analysis**
![Screenshot 2025-03-24 152108](https://github.com/user-attachments/assets/8ed3471b-4f58-4827-ba2e-34a4ac3a3b04)

---
###**5. Bonous Question**
### **Circuit 1**
**DC analysis**
 
### **Circuit 3**
## **Using 500nm technology**

| *Parameters*  | *M1*   | *M2*   | *M3*       |
| ------------- | ------ | ------ | ---------- |
| **Model**     | CMOSP  | CMOSP  | CMOSN      |
| **Length (m)**| 500n   | 500n   | 500n       |
| **Width (m)** | 100u    | 100u    | 61u  |
| **Current (A)**| 0.2777m| 0.2777m| 0.2777m    |
### **AC Analysis**
- For \( L = 180nm \), gain \( A_v \) is approximately **10.5 V/V**.  
- For \( L = 500nm \), gain \( A_v \) is approximately **28.475 V/V**.  

**Gain Calculation Formula:**

\[
A_v = \frac{V_{out}}{V_{in}}
\]

**Example Calculation:**

\[
A_v = \frac{(1.632 - 0.154)}{(770m - 630m)}
\]

- Gain (dB) for \( L = 500nm \) is approximately **34.11 dB**.  
- **3dB Bandwidth** = *75.752 MHz*.  

---

### **Transient Analysis**
- Output gain is approximately **28.475 V/V** for \( L = 500nm \).

---

## **6. Bonus Question**
- *How does increasing the channel length affect the output impedance of the current mirror?*

---

## **Circuit Diagrams**
*(Include images of the circuit configurations here)*
