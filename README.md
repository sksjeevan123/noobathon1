<img width="905" height="823" alt="Screenshot 2026-02-22 015642" src="https://github.com/user-attachments/assets/972b6f91-26e6-4714-a0fe-ae2817a6577b" /><img width="905" height="823" alt="Screenshot 2026-02-22 015642" src="https://github.com/user-attachments/assets/5a412cd6-aa08-485d-8ccf-0cdd774bed0a" /><img width="905" height="823" alt="Screenshot 2026-02-22 015642" src="https://github.com/user-attachments/assets/b2916bea-77da-4ad1-b30f-79db17a620e4" /><img width="905" height="823" alt="Screenshot 2026-02-22 015642" src="https://github.com/user-attachments/assets/65269f9b-89b6-4280-8319-d03831005ce0" /><img width="905" height="823" alt="Screenshot 2026-02-22 015642" src="https://github.com/user-attachments/assets/9d2f2a55-6491-4e8c-b5fc-35db654c5413" /><img width="905" height="823" alt="Screenshot 2026-02-22 015642" src="https://github.com/user-attachments/assets/bf0e702a-25c0-4651-8618-c2302becb8a4" /><img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/ff4fedd5-1836-4e5c-835f-28ccb1bb7fde" 
                                                                                                                                                             
A real-time disaster management and resource tracking system built for the Noobathon .

## 🚀 Overview

This system helps coordinate disaster response by tracking infection rates and resource allocation across different sectors. It provides real-time data visualization and management capabilities for emergency responders.

## 📊 Key Features

### 1. Sector Management
- Track multiple sectors/zones in the disaster area
- Monitor infection rates per sector
- View historical infection data

### 2. Resource Tracking
- Real-time resource inventory management
- Track essential supplies:
  - 💊 Medical supplies
  - 🍲 Food packets
  - 💧 Water bottles
  - 🏕️ Tents
  - 👕 Blankets

### 3. Analytics Dashboard
- Infection rate trends over time
- Resource allocation visualization
- Sector-wise data comparison
- Historical data tracking

## 🛠️ Technology Stack

### Backend
- **Node.js** - Runtime environment
- **Express** - Web framework
- **MongoDB** - Database
- **Mongoose** - ODM for MongoDB
- **dotenv** - Environment variable management

### Frontend (GitHub Pages)
- HTML5/CSS3
- JavaScript
- Chart.js for visualizations

## 📡 API Endpoints

### Public Endpoints
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/` | Main server status page |
| GET | `/api/test` | Test endpoint |
| GET | `/api/health` | Server health check |
| GET | `/api/debug/users` | Debug user data |

### Data Endpoints
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/sectors` | Get list of all sectors |
| GET | `/api/infection-history/:sector` | Get infection data for a sector |
| GET | `/api/resource-data/:sector` | Get resource data for a sector |

### Admin Endpoints
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/admin/sample-infection` | Add sample infection data |
| POST | `/api/admin/sample-resources` | Add sample resource data |

## 📦 Data Models

### Infection Record
```javascript
{
  sector: String,      // Sector name/ID
  date: Date,          // Date of record
  infectionRate: Number // Rate (0-100%)
}
