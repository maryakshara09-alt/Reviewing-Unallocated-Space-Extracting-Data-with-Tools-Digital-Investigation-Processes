# Reviewing-Unallocated-Space-Extracting-Data-with-Tools-Digital-Investigation-Processes
## AIM:
To review unallocated space in a disk image, extract data using forensic tools, and understand the digital investigation process.
## REQUIREMENTS
- Autopsy or FTK Imager
- Sleuth Kit (TSK)
- Hex Editor (e.g., HxD)
- Operating System: Windows 10/11 or Linux (Kali preferred)
## ARCHITECTURE DIAGRAM
```mermaid
flowchart TD
    A[Disk Image / Physical Drive] --> B[Load into Autopsy or Sleuth Kit]
    B --> C[Identify Unallocated Space]
    C --> D[Scan for Data Signatures]
    D --> E[Carve and Recover Files]
    E --> F[Analyze Recovered Data]
    F --> G[Document Findings in Report]
```
## DESIGN STEPS:
### Step 1 (Acquire Evidence Image):
- Obtain the disk image in ```.dd``` or ```.E01``` format from a trusted forensic acquisition process.
- Verify hash values (MD5/SHA256) to maintain integrity.

### Step 2(Load Image into Forensic Tool):
- Open Autopsy or FTK Imager.
- Create a new case and add the evidence image.

### Step 3(Locate Unallocated Space):
- Navigate to the partition structure view.
- Identify sectors not assigned to any partition (unallocated).
### Step 4(Analyze & Carve Data):
- Use built-in data carving tools to search for file signatures (JPEG, DOCX, PDF, etc.).
- Preview carved files for relevance.
  
## PROGRAM:
| Step | Action                     | Tool Used                   | Output                       |
| ---- | -------------------------- | --------------------------- | ---------------------------- |
| 1    | Load disk image            | Autopsy / FTK Imager        | Partition & unallocated view |
| 2    | Identify unallocated space | Autopsy File System View    | Sector ranges                |
| 3    | Data carving               | Autopsy Data Carving Module | Recovered files              |
| 4    | Export evidence            | Autopsy Export Option       | File copies for analysis     |


## OUTPUT:
Unallocated Space Analysis and Extracted Data Report
<img width="906" height="512" alt="Screenshot 2026-11-16 134721" src="https://github.com/user-attachments/assets/7d4e4f20-bc61-447e-8499-fd09878088e1" />
<img width="1127" height="605" alt="Screenshot 2026-11-16 134730" src="https://github.com/user-attachments/assets/25e0fed2-dcf3-458a-bf03-7c095048bf25" />

<img width="1130" height="671" alt="Screenshot 2026-11-16 134740" src="https://github.com/user-attachments/assets/8ef68096-71ef-4f0e-aff4-699f9871d5d1" />

<img width="1140" height="712" alt="Screenshot 2026-11-16 134752" src="https://github.com/user-attachments/assets/d2af0dc5-837b-48af-82b8-84736ad6b3fe" />

<img width="1137" height="696" alt="Screenshot 2026-11-16 134805" src="https://github.com/user-attachments/assets/ecad504d-9a7c-43e7-a3fb-e5d560e9f672" />

<img width="1145" height="597" alt="Screenshot 2026-11-16 134817" src="https://github.com/user-attachments/assets/182ff739-045a-460b-a382-3f578d474da2" />

<img width="1041" height="568" alt="Screenshot 2026-11-16 134824" src="https://github.com/user-attachments/assets/d7a58dc9-5aae-427d-b4e6-62156de57830" />

<img width="1068" height="687" alt="Screenshot 2026-11-16 134835" src="https://github.com/user-attachments/assets/04d3cd04-62d5-42f7-87c0-3afaf208f6f3" />

## RESULT:
The unallocated space was successfully analyzed, data was extracted, and the digital investigation process was followed effectively.

