## System Architecture

PrimePC ใช้สถาปัตยกรรมแบบ **3-Tier Architecture** โดยแบ่งระบบออกเป็น 3 ส่วนหลัก ได้แก่ Frontend, Backend และ Database เพื่อให้ระบบมีโครงสร้างที่ชัดเจน สามารถพัฒนา ดูแลรักษา และขยายระบบในอนาคตได้ง่าย

```mermaid
flowchart TB

subgraph Client
    A[Customer]
end

subgraph Frontend
    B[Web Browser<br/>HTML CSS JavaScript]
end

subgraph Backend
    C[Web Server<br/>Node.js / Express]
    D[REST API]
end

subgraph Database
    E[(Users)]
    F[(Products)]
    G[(Orders)]
end

A --> B
B --> C
C --> D

D --> E
D --> F
D --> G
```