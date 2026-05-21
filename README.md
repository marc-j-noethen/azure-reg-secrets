# azure-reg-secrets

Security Gatekeeper Pipeline
This repository contains a GitHub Actions workflow that automatically builds Docker images, scans them for critical vulnerabilities using Trivy, and only pushes them to an Azure Container Registry (ACR) if the scan is clean.
What happens with every push?

The Docker image is built
Trivy scans the image for critical CVEs
The image is uploaded to the ACR only if no critical findings are detected

This automatically blocks insecure images before they reach the registry.