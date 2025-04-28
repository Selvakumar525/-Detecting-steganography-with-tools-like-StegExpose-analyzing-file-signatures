# Detecting-steganography-with-tools-like-StegExpose-analyzing-file-signatures
## AIM:
To detect hidden data using steganography detection tools like StegExpose and analyze file signatures for authenticity and manipulation.

## DESIGN STEPS:
### Step 1:
Install StegExpose or use the JAR version to detect steganography in image files.

### Step 2:
Run StegExpose on a directory of suspected image files using the command:

### Step 3:
Analyze file signatures using tools like file, binwalk, or xxd to check for inconsistencies or embedded content.

## PROGRAM:
- **Install and Verify Steghide Tool**
  ```bash
  sudo apt update
  sudo apt install steghide
  steghide --version 
  ```
- **Embed the Secret Message into the Image** 
  ```bash
  steghide embed -cf image.jpg -ef hidden.txt
  ```

- **Extract the Hidden Secret from Image and Verify the Extracted Message**
  ```bash
  steghide extract -sf image.jpg
   cat hidden.txt
  ```

- **Retrieve Information About the Embedded Data**
  ```bash
   steghide info image.jpg
  ```

- **Analyze File Signature**
  ```bash
    file image.jpg
    binwalk image.jpg
  ```
 
## OUTPUT:
### Install and Verify Steghide Tool
![image](https://github.com/user-attachments/assets/3719303e-1517-48f5-ab66-ee9cdf314759)

### Embed the Secret Message into the Image
![image](https://github.com/user-attachments/assets/79225ae9-2b35-418d-ae24-f74666bbfac4)

### Delete Original Secret File
![image](https://github.com/user-attachments/assets/b9113453-d7dc-4966-9363-3bfdd4508cbb)

###  Extract the Hidden Secret from Image
![image](https://github.com/user-attachments/assets/074bbf4b-62d3-4fd7-8e59-2c11e545589c)

### Verify the Extracted Message
![image](https://github.com/user-attachments/assets/62e8d489-5d95-4ff8-aa48-dde4ff1505b3)

### Retrieve Information About the Embedded Data
![image](https://github.com/user-attachments/assets/ff2745b2-8e63-4504-bc67-3c7044237ee7)

### Analyze File Signature
![image](https://github.com/user-attachments/assets/4a6e6b49-2b8d-4a82-92b0-ebae90f8f998)

## RESULT:
Hidden data was successfully detected and file signatures were analyzed for irregularities.
