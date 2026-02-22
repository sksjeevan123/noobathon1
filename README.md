<video src="./videoscreen.mp4" controls controlsList="nodownload"></video>
                                                                                                                                                             
A real-time disaster management and resource tracking system built for the Noobathon .

  Overview

This system helps coordinate disaster response by tracking infection rates and resource allocation across different sectors. It provides real-time data visualization and management capabilities for emergency responders.

 Key Features

 1. Sector Management
- Track multiple sectors/zones in the disaster area
- Monitor infection rates per sector
- View historical infection data

 2. Resource Tracking
- Real-time resource inventory management
- Track essential supplies:
  -  Medical supplies
  -  Food packets
  -  Water bottles
  -  Tents
  -  Blankets

 3. Analytics Dashboard
- Infection rate trends over time
- Resource allocation visualization
- Sector-wise data comparison
- Historical data tracking

 Technology Stack

 Backend
- **Node.js** - Runtime environment
- **Express** - Web framework
- **MongoDB** - Database
- **Mongoose** - ODM for MongoDB
- **dotenv** - Environment variable management

 Frontend (GitHub Pages)
- HTML5/CSS3
- JavaScript
- Chart.js for visualizations

 📡 API Endpoints

 Public Endpoints
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/` | Main server status page |
| GET | `/api/test` | Test endpoint |
| GET | `/api/health` | Server health check |
| GET | `/api/debug/users` | Debug user data |

 Data Endpoints
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/sectors` | Get list of all sectors |
| GET | `/api/infection-history/:sector` | Get infection data for a sector |
| GET | `/api/resource-data/:sector` | Get resource data for a sector |

 Admin Endpoints
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/admin/sample-infection` | Add sample infection data |
| POST | `/api/admin/sample-resources` | Add sample resource data |

 Data Models

 Infection Record
```javascript
{
  sector: String,      // Sector name/ID
  date: Date,          // Date of record
  infectionRate: Number // Rate (0-100%)
}
