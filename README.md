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

(---

## 📦 Why `go.mod` Is Required in Go Workflows

Go uses a module system to manage dependencies and organize code. The `go.mod` file is the manifest that tells Go:

- What the module name is (usually your repo path)
- What dependencies your project uses
- What Go version you're targeting

Without `go.mod`, Go doesn't know how to resolve imports or where your code starts. So when GitHub Actions runs `go test ./...`, it looks for a module and fails with:

> `pattern ./...: directory prefix . does not contain main module or its selected dependencies`

---

## 🛠️ What `go mod init` Does

When you run:

```bash
go mod init github.com/<your-username>/<your-repo-name>

It creates a go.mod file like this:

module github.com/your-username/your-repo-name

go 1.21
)



****3. Docker Build Workflow (docker-build.yml)****
->Trigger: Runs on push only if:
->Dockerfile changes
->Files inside app/ change
->Actions:
->Builds Docker image
->Use Case: Automates Docker builds for deployment
