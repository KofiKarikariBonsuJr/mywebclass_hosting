# 🚀 MyWebClass Hosting Platform

**Modern Docker-based web hosting for CS students**

This repository provides a complete, production-ready web hosting platform designed for Computer Science education. Students learn modern DevOps practices while hosting their own websites with automatic SSL certificates.

## 🎯 What You'll Learn

- **Docker & Containerization** - Industry-standard deployment
- **Reverse Proxy** - Load balancing and routing with Caddy
- **SSL/TLS Security** - Automatic HTTPS with Let's Encrypt
- **Domain Management** - DNS configuration and subdomains
- **Git Workflows** - Version control and deployment
- **System Administration** - Linux server management
- **Web Security** - Firewall, monitoring, and best practices

## 🏗️ Architecture

```
Internet → Caddy (Reverse Proxy + SSL) → Your Web Applications
           ↓
       Auto SSL Certificates (Let's Encrypt)
```

## 📚 Repository Structure

```
hosting/
├── caddy/                  # Reverse proxy configuration
│   ├── Caddyfile          # Main routing configuration
│   ├── docker-compose.yml # Caddy container setup
│   └── data/              # SSL certificates & config
├── templates/             # Student project templates
│   ├── static-site/       # HTML/CSS/JS websites
│   ├── nodejs-app/        # Node.js applications
│   ├── python-flask/      # Python web apps
│   └── react-app/         # React applications
├── examples/              # Working example projects
├── docs/                  # Detailed documentation
│   ├── getting-started.md # Quick setup guide
│   ├── deployment.md      # How to deploy apps
│   ├── ssl-setup.md       # SSL certificate management
│   ├── troubleshooting.md # Common issues & solutions
│   └── advanced.md        # Advanced configurations
├── scripts/               # Utility scripts
│   ├── setup.sh           # Initial server setup
│   ├── deploy.sh          # Application deployment
│   └── ssl-check.sh       # SSL certificate monitoring
└── README.md              # This file
```

## ⚡ Quick Start

### 1. Clone Repository
```bash
git clone git@github.com:kaw393939/mywebclass_hosting.git
cd mywebclass_hosting
```

### 2. Initial Setup
```bash
./scripts/setup.sh
```

### 3. Deploy Your First Site
```bash
# Copy a template
cp -r templates/static-site/ my-website/
cd my-website/
# Edit your content
./deploy.sh
```

### 4. Configure Domain
Add your domain to `caddy/Caddyfile`:
```
yourdomain.com {
    reverse_proxy my-website:80
}
```

### 5. Start Services
```bash
cd caddy/
docker compose up -d
```

🎉 **Your website is now live with automatic HTTPS!**

## 🛡️ Security Features

- ✅ **Automatic SSL** - Let's Encrypt certificates
- ✅ **Firewall Protection** - UFW configured
- ✅ **SSH Security** - Key-based authentication
- ✅ **Container Isolation** - Docker security
- ✅ **Monitoring** - System health checks
- ✅ **Auto-Updates** - Security patches

## 🎓 Learning Paths

### **Beginner Level**
1. Deploy a static HTML website
2. Configure custom domain
3. Understand SSL certificates
4. Basic Docker commands

### **Intermediate Level**  
1. Deploy Node.js/Python applications
2. Database integration
3. Environment variables
4. Multiple applications

### **Advanced Level**
1. Load balancing multiple instances
2. CI/CD with GitHub Actions  
3. Monitoring and logging
4. Performance optimization

## 📖 Documentation

- [📋 Getting Started Guide](docs/getting-started.md)
- [🚀 Deployment Guide](docs/deployment.md)
- [🔒 SSL Setup](docs/ssl-setup.md)
- [🔧 Troubleshooting](docs/troubleshooting.md)
- [⚙️ Advanced Configuration](docs/advanced.md)

## 💡 Example Projects

- **Portfolio Website** - Showcase your projects
- **Blog Platform** - Share your thoughts
- **API Service** - Build REST APIs
- **Real-time Chat** - WebSocket applications
- **E-commerce Site** - Online store

## 🤝 Contributing

This is an educational platform - students are encouraged to:
- Submit improvements via Pull Requests
- Share example projects
- Report issues and suggest features
- Help fellow students in discussions

## 📝 License

MIT License - Free for educational and commercial use

## 🆘 Support

- **GitHub Issues** - Bug reports and questions
- **Discussions** - Community help and sharing
- **Wiki** - Additional tutorials and guides

---

**Built for CS Education | Maintained by Professor Williams**

*Empowering students to learn modern web hosting and DevOps practices*