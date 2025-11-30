# AUTO-CORRELATION-AND-PSD

## **Aim**
Write a program for **Autocorrelation** and **Power Spectral Density (PSD)** of signals in **Scilab** and verify the **Wiener–Khinchin relation**.

---

## **Equipments Needed**
- Computer with **Intel i3 processor** (or higher)  
- **Scilab** software

---

## **Theory**
The **Wiener–Khinchin theorem** states that:  
> The Power Spectral Density (PSD) of a wide-sense stationary random process is the **Fourier Transform** of its **autocorrelation function**.
<img width="466" height="74" alt="image" src="https://github.com/user-attachments/assets/f7c7673b-e086-4231-b8b4-4a677a3f7d0c" />

This relationship bridges the **time-domain correlation** and **frequency-domain power** representations of a signal.

---

## **Algorithm**
1. **Load or Define the Signal:** Input your time-domain signal.  
2. **Compute Autocorrelation:** Calculate the autocorrelation function of the signal.  
3. **Compute Power Spectral Density (PSD):**  
   Estimate the PSD using either:  
   - Fourier Transform of the autocorrelation function, or  
   - Methods like Welch’s periodogram.  
4. **Plot Results:** Visualize both the autocorrelation function and PSD.

---

## **Procedure**
1. Refer to the algorithm and write the code for the experiment.  
2. Open **Scilab** on your system.  
3. Type your code in a **new editor**.  
4. **Save** the file.  
5. **Execute** the code.  
6. If any errors occur, **debug and re-run** the program.  
7. Verify the generated waveform using **tabulation** and **model waveform** comparison.

---

## **Program (Scilab Code)**

```scilab
t = 0:0.01:2*%pi;
x = sin(2*t);

subplot(3,2,1);
plot(x);

au = xcorr(x, x);
subplot(3,2,2);
plot(au);

v = fft(au);
subplot(3,2,3);
plot(abs(v));

fw = fft(x);
subplot(3,2,4);
plot(fw);

fw2 = (abs(fw)).^2;
subplot(3,2,5);
plot(fw2);
```
---
## **Output:**

<img width="808" height="749" alt="image" src="https://github.com/user-attachments/assets/bd76ad06-9bbc-481d-84d7-3eeb0b68f792" />


![WhatsApp Image 2025-11-30 at 14 22 50_2289484b](https://github.com/user-attachments/assets/f4653ec1-cb2a-4f84-a6ae-de39c219db4e)
---

## **Result:**
Thus the Autocorrelation and PSD are executed in Scilab and output is verified.

---
