# FILE-RECOVERY-USING-AUTOPSY-SOFTWARE

## AIM
To use **Autopsy Digital Forensics Tool** to retrieve deleted files from a disk image.

---

## REQUIREMENTS
- **Operating System**: Windows 10/11, macOS, or Linux
- **Tool**: [Autopsy Digital Forensics](https://www.autopsy.com/)  
- **Test Data**: Disk image file (`disk.dd`, `disk.img`, `.E01`)

---

## ARCHITECTURE DIAGRAM
```mermaid
flowchart TD
    A[Disk Image / Physical Drive] --> B[Install Autopsy]
    B --> C[Create New Case in Autopsy]
    C --> D[Add Data Source: Disk Image]
    D --> E["Run File System & Data Recovery Modules"]
    E --> F[Locate Deleted Files in Results]
    F --> G[Recover and Export Deleted Files]
```
## DESIGN STEPS:
### Step 1:
Open Autopsy and create a new case with appropriate case details.

### Step 2:
Add a disk image as a data source and let Autopsy analyze the content.

### Step 3:
Navigate to the "Deleted Files" section in Autopsy and examine or recover the deleted files.

## PROGRAM:
### Install Autopsy
```bash
# Download Autopsy from:
# https://www.autopsy.com/
# Install following the setup wizard.
```
### Create a New Case
```
# File → New Case
# Enter Case Name: Deleted_File_Recovery
# Choose Base Directory: C:\Cases\Deleted_File_Recovery
# Click Finish
```
### Add Disk Image
```
# Add Data Source → Disk Image or VM File
# Browse to: C:\forensics\disk.dd
# Click Next
```
### Run Ingest Modules
```# Select:
# - File System Analysis
# - Keyword Search (optional)
# - Data Recovery / Carving
# Click Finish
```
### Locate Deleted Files
```
# Navigate to 'Deleted Files' section in the tree view
# Review metadata (size, hash, timestamps)
```
### Export Deleted Files
```
# Right-click → Extract File(s)
# Save to: C:\forensics\Recovered_Files\
```

## OUTPUT:
Recovered Deleted File List and Details
<img width="1920" height="1200" alt="Screenshot 2026-11-02 121933" src="https://github.com/user-attachments/assets/89293b1c-d11c-4772-9b43-be30ac4f81f5" />
<img width="1920" height="1140" alt="Screenshot 2026-11-02 130445" src="https://github.com/user-attachments/assets/1293f769-1e94-48a4-919c-ba492fbf9c8a" />
<img width="1920" height="1140" alt="Screenshot 2026-11-02 130514" src="https://github.com/user-attachments/assets/7b5dda80-9bba-40de-af04-c19c73301e4b" />
<img width="1920" height="1200" alt="Screenshot 2026-11-02 130529" src="https://github.com/user-attachments/assets/57e1cd19-bbd0-4f4a-8576-a2d2bc60bcc4" />
<img width="1920" height="1200" alt="Screenshot 2026-11-02 131107" src="https://github.com/user-attachments/assets/e0bdca90-aa8e-464a-99ab-7e981aa8be3a" />
<img width="1920" height="1200" alt="Screenshot 2026-11-02 131126" src="https://github.com/user-attachments/assets/4282c442-7b28-41ba-8c04-96b7fa5ee113" />
<img width="1920" height="1200" alt="Screenshot 2026-11-02 131136" src="https://github.com/user-attachments/assets/4335ef37-ffd8-4787-a27e-9260cd4ee693" />
<img width="1920" height="1200" alt="Screenshot 2026-11-02 131147" src="https://github.com/user-attachments/assets/9e9264c3-9c34-4fa9-8992-095bad6569f8" />
<img width="1920" height="1200" alt="Screenshot 2026-11-02 131314" src="https://github.com/user-attachments/assets/1c75697f-161b-4565-9a2d-fbdf1e20dc0c" />
<img width="1920" height="1140" alt="Screenshot 2026-11-02 131331" src="https://github.com/user-attachments/assets/9c6e2444-6d17-47ba-b16a-41f45066d01e" />
<img width="1920" height="1140" alt="Screenshot 2026-11-02 131344" src="https://github.com/user-attachments/assets/f783ce92-d903-49bb-b465-401f292d673d" />
<img width="1920" height="1200" alt="Screenshot 2026-11-02 131421" src="https://github.com/user-attachments/assets/af0e47dc-dc50-4982-90b0-95711dbc0da1" />
<img width="1920" height="1200" alt="Screenshot 2026-11-02 131433" src="https://github.com/user-attachments/assets/8b7b5649-3306-4a87-9e65-a026230d4443" />
<img width="1920" height="1140" alt="image" src="https://github.com/user-attachments/assets/bcd154b9-8866-4fa9-a438-f3061e9899d3" />

## RESULT:
Deleted files were successfully retrieved and analyzed using Autopsy.
