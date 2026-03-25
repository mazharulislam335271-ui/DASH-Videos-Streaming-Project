# DASH Video Streaming Project

## 📌 Overview
This project presents the implementation and evaluation of a Dynamic Adaptive Streaming over HTTP (DASH) system in a controlled virtual environment. The objective is to analyze how different network conditions affect video streaming performance and Quality of Experience (QoE). The system uses adaptive bitrate streaming to dynamically adjust video quality based on available bandwidth.

---

## 🛠️ Tools & Technologies
- FFmpeg (video encoding and processing)
- DASH (MPD manifest and segmentation)
- Apache Web Server (content delivery)
- iPerf (network traffic testing)
- Linux Traffic Control (tc)
  - Token Bucket Filter (TBF)
  - Hierarchical Token Bucket (HTB)
  - Traffic Policing

---

## 🎬 Video Processing

### FFmpeg Installation
![FFmpeg](screenshots/Setup_FFmpeg.png)

### Transcoding (1.5 Mbps, 2 Mbps, 4 Mbps)
![Transcoding](screenshots/Transcoding.png)

---

## 📦 DASH Packaging

### DASH Manifest and Segments
![DASH1](screenshots/DASH_1.png)
![DASH2](screenshots/DASH_2.png)

---

## 🌐 Web Server Configuration

### Apache Server Setup
![Server](screenshots/server_1.png)

### DASH URLs Access
![URL1](screenshots/unique_url_1.png)
![URL2](screenshots/unique_url_2.png)

---

## 📊 Network Testing

### iPerf Implementation
![iPerf](screenshots/IPREF.png)

### Bandwidth Testing
![Bandwidth](screenshots/Bandwidth.png)

---

## ⚙️ Traffic Control Implementation

### Token Bucket Filter (TBF)
- Rate: 2.5 Mbps  
- Burst: 20 KB  
- Latency: 50 ms  

![TBF](screenshots/TBF.png)

---

### Hierarchical Token Bucket (HTB)
- Minimum Rate: 2.5 Mbps  
- Maximum Rate: 5 Mbps  

![HTB](screenshots/HTB.png)

---

### Traffic Policing
- Rate Limit: 3.5 Mbps  
- Excess traffic is dropped  

![Policing](screenshots/TPI.png)

---

## ▶️ Final Output

### DASH Video Playback
![Playback](screenshots/playBack.png)

---

## 📈 Results & Observations
- DASH successfully adapts video quality based on available bandwidth.
- Under TBF, video quality reduces slightly but playback remains smooth.
- HTB provides better performance due to flexible bandwidth allocation.
- Traffic policing causes packet loss, leading to buffering and poor QoE.
- Packet loss has a more severe impact on streaming compared to bandwidth limitation.

---

## 🚀 How to Run the Project

1. Install FFmpeg on the server.
2. Download and verify input videos.
3. Transcode videos into multiple bitrates.
4. Generate DASH MPD and segments.
5. Configure Apache server to host content.
6. Apply traffic control rules using `tc`.
7. Use iPerf to generate network traffic.
8. Access DASH stream via browser.

---

## 👤 Author
Ashir
