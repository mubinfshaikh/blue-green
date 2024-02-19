# Path-Based Routing Demo with Docker, Kubernetes, and Ingress

This project demonstrates how to achieve path-based routing using Docker, Kubernetes, and Ingress controller. It includes two HTML files, `green.html` and `blue.html`, each serving a different page content. When accessing specific paths, the appropriate HTML file is served.

## Prerequisites

Make sure you have the following tools installed and configured:

- Docker
- Kubernetes
- Ingress controller (e.g., Nginx Ingress Controller)

## Getting Started

1. Clone this repository to your local machine:

```bash
git clone https://github.com/mubinfshaikh/k8s-ingress-pathbased-routing.git
cd k8s-ingress-pathbased-routing
```
2. Build the Docker image:
   ```
   docker build -t nginx-blue-green .
   ```
3. Deploy the Docker image to your Kubernetes cluster:
   ```
   kubectl apply -f kubernetes/deployment.yml
   ```
4. Deploy ingress to your kubernetes cluster:
   ```
   kubectl apply -f kubernetes/ingress.yml
   ```

Usage
Once the setup is complete, you can access the following URLs:

http://yourdomain.com/green - Welcome to the Green Page (served by green.html)
http://yourdomain.com/blue - Welcome to the Blue Page (served by blue.html)

License
This project is licensed under the MIT License.

