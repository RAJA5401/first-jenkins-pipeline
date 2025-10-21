# Jenkins Node.js Pipeline 🚀

This project contains a sample **Jenkins Declarative Pipeline** using a **Docker agent** with Node.js.

### Pipeline Stages
1. **Install Dependencies** – runs `npm install`
2. **Run Tests** – executes test cases (if available)
3. **Build App** – builds your Node.js app
4. **Docker Build** – builds a Docker image with Jenkins

### How I Customized It
- Added multiple stages for a complete CI pipeline
- Used `node:16-alpine` Docker image
- Included post actions for success/failure

Inspired by a base pipeline but expanded for learning Jenkins + Docker CI/CD.

