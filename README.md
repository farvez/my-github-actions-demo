# my-github-actions-demo
A demo repository showcasing multiple GitHub Actions workflows including basic automation, Go testing, and Docker image builds. Ideal for learning CI/CD with real-time examples.

**1. Basic Workflow (basic.yml)**
-> Trigger: Runs on every push
-> Actions:
-> Checks out code
-> Prints “Hello from GitHub Actions!”
-> Use Case: Great for beginners to test basic automation
**2. Go Tests Workflow (go-tests.yml)**
-> Trigger: Runs on every push
-> Actions:
-> Sets up Go (v1.21)
->Runs go test on all packages
->Use Case: Automates testing for Go projects
**3. Docker Build Workflow (docker-build.yml)**
->Trigger: Runs on push only if:
->Dockerfile changes
->Files inside app/ change
->Actions:
->Builds Docker image
->Use Case: Automates Docker builds for deployment
