# 🚀 Refund Status Demo Pro++ - User Guide

## 📋 What You Need
- **Docker Desktop** installed on your machine
- **3 files** from the distribution package:
  - `refund-status-demo-pro-plus.tar` (Docker image)
  - `docker-compose.dist.yml` (Deployment config)
  - `README.md` (Full documentation)

## 🎯 Quick Start (3 Steps)

### Step 1: Load the Docker Image
```bash
docker load -i refund-status-demo-pro-plus.tar
```

### Step 2: Start the Application
```bash
docker compose -f docker-compose.dist.yml up -d
```

### Step 3: Access the Application
- **Frontend**: http://localhost:8080
- **API Documentation**: http://localhost:8000/docs
- **Health Check**: http://localhost:8000/healthz

## 🛑 Stop the Application
```bash
docker compose -f docker-compose.dist.yml down
```

## 🔍 Check Application Status
```bash
docker compose -f docker-compose.dist.yml ps
```

## 📊 What's Included
This single Docker image contains:
- ✅ **Frontend**: React application with TypeScript
- ✅ **Backend**: FastAPI server with Python
- ✅ **Database**: SQLite (no external dependencies)
- ✅ **AI Services**: Template-based LLM responses
- ✅ **Caching**: In-memory cache system

## 🌐 Features
- **Refund Status Tracking**: Check IRS refund status
- **ETA Predictions**: AI-powered refund timing estimates
- **AI Guidance**: Intelligent advice based on status
- **Responsive UI**: Modern, mobile-friendly interface
- **API Access**: Full REST API for integration

## 🔧 Configuration
The application comes pre-configured for demo use:
- **IRS Simulation**: Configurable health states (healthy/degraded/down)
- **Mock Data**: Sample refund scenarios for testing
- **Demo Mode**: Safe for demonstration and testing

## 🚨 Troubleshooting

### Application Won't Start
```bash
# Check Docker is running
docker --version

# Check image is loaded
docker images | grep refund-status-demo-pro-plus

# View logs
docker compose -f docker-compose.dist.yml logs
```

### Port Already in Use
If ports 8080 or 8000 are busy, edit `docker-compose.dist.yml`:
```yaml
ports:
  - "8081:80"    # Change 8080 to 8081
  - "8001:8000"  # Change 8000 to 8001
```

### Permission Issues
On Linux/macOS, you might need:
```bash
sudo docker load -i refund-status-demo-pro-plus.tar
sudo docker compose -f docker-compose.dist.yml up -d
```

## 📞 Support
If you encounter issues:
1. Check this user guide
2. Review the full README.md
3. Check Docker logs: `docker compose -f docker-compose.dist.yml logs`
4. Verify Docker is running: `docker info`

## 🎉 Success!
When everything is working:
- ✅ Frontend loads at http://localhost:8080
- ✅ API responds at http://localhost:8000
- ✅ You can submit forms and see responses
- ✅ API documentation is accessible

---

**Note**: This is a demo application with mock data. It's not connected to real IRS systems.
