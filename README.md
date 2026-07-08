# 📱 UPI QR Code Generator using Python

## 📖 Project Overview

The **UPI QR Code Generator** is a simple Python project that creates QR codes for UPI payments. It allows users to enter their UPI ID and automatically generates QR code images that can be scanned using popular UPI payment applications such as **PhonePe**, **Google Pay**, and **Paytm**.

This project is ideal for beginners who want to learn how QR code generation works using Python. It demonstrates the use of user input, string formatting, the `qrcode` library, image generation, and file handling.

---

## ✨ Features

- Accepts a UPI ID from the user.
- Generates QR codes for:
  - 📱 PhonePe
  - 📱 Google Pay
  - 📱 Paytm
- Saves each QR code as a PNG image.
- Automatically opens the generated QR code images.
- Beginner-friendly and easy-to-understand Python code.

---

## 🛠️ Technologies Used

- Python 3.x
- qrcode Library
- Pillow (PIL)

---

## 📥 Installation

### Step 1: Clone the Repository

```bash
git clone https://github.com/your-username/UPI-QR-Code-Generator.git
```

### Step 2: Navigate to the Project Folder

```bash
cd UPI-QR-Code-Generator
```

### Step 3: Install the Required Library

```bash
pip install qrcode[pil]
```

---

## ▶️ How to Run

Run the Python program:

```bash
python qr_generator.py
```

When prompted, enter your UPI ID.

**Example:**

```
Enter your UPI Id:
sakshi@oksbi
```

The program will:

- Generate PhonePe QR Code
- Generate Google Pay QR Code
- Generate Paytm QR Code
- Save them as PNG files
- Open the QR codes automatically

---

## 💻 Source Code

```python
import qrcode

upi_id = input("Enter your UPI Id: ")

# URLs based on the UPI ID and payment apps
phonepe_url = f"upi://pay?pa={upi_id}&pn=Recipient%20Name"
google_pay_url = f"upi://pay?pa={upi_id}&pn=Recipient%20Name"
paytm_url = f"upi://pay?pa={upi_id}&pn=Recipient%20Name"

# Create QR Code for each payment app
phonepe_qr = qrcode.make(phonepe_url)
google_pay_qr = qrcode.make(google_pay_url)
paytm_qr = qrcode.make(paytm_url)

# Save QR Codes
phonepe_qr.save("phonepe_qr.png")
google_pay_qr.save("google_pay_qr.png")
paytm_qr.save("paytm_qr.png")

# Display QR Codes
phonepe_qr.show()
google_pay_qr.show()
paytm_qr.show()
```

---

## 📸 Output Files

After running the program, the following files will be created:

```
phonepe_qr.png
google_pay_qr.png
paytm_qr.png
```

These QR codes contain the same UPI payment information and can be scanned by any UPI-supported payment application.

---

## 🔄 Project Workflow

1. Import the `qrcode` library.
2. Accept the UPI ID from the user.
3. Create UPI payment URLs.
4. Generate QR codes.
5. Save QR codes as PNG images.
6. Display the generated QR codes.

---

## 📚 Concepts Used

- Python Input & Output
- Variables
- String Formatting (f-Strings)
- Functions
- QR Code Generation
- Image Processing

---

## 🔍 Sample UPI URL

```
upi://pay?pa=sakshi@oksbi&pn=Recipient%20Name
```

### URL Parameters

| Parameter | Description |
|-----------|-------------|
| `pa` | Payee UPI ID |
| `pn` | Payee Name |

---

## ⚠️ Notes

- Enter a valid UPI ID for the QR code to work correctly.
- The generated QR codes follow the standard UPI payment URI format.
- Although separate QR images are generated for PhonePe, Google Pay, and Paytm, they contain the same UPI payment information and can usually be scanned by any UPI-compatible payment app.

---

## 🚀 Future Enhancements

- Add payment amount.
- Add transaction note.
- Add merchant name.
- Add transaction reference number.
- Design a graphical user interface (GUI).
- Generate customized QR codes with colors and logos.
- Export QR codes in different image formats.

