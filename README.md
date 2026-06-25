# Interview_Questions
# Sirius-BI Questions<br></br>
# Round 1
Q1: Ma jata hu aur website ka naam likhta hu but its not reachable but when I type ip it is reachable?<br></br>
Q2: AWS scretes management?<br></br>
Q3: Abhi service aik vendor provide kr rha ha but unho nay services ko apney infra pay shift karna ha tou kaisey karein ge?<br></br>
A: Blue, Green Deployment Concept<br></br>
Q4: Aik container chal rha ha aur wo container memory aur cpu boht ziada use kr rha ha aur mainey usey constraint karna ha?<br></br>
A: Resource Limit and Resource Usage Concept in Kubernetes<br></br>
Q5: lambda function kay ander aik cheez hoti ha forget wo kia hoti ha?<br></br>
A: Jo lambda functions chal rhy hotey hain un may aik time function/constraint hotey hain usey forget boltey hain (is question ko gpt say aur verify karein)<br></br>
Q6: What is the difference between and add and copy in dockerfile?<br></br>
A: COPY just copies files from the local system into the image, while ADD can also extract archives and download files from URLs. In practice, COPY is preferred because it is more predictable.<br></br>
Q7: Sometimes pipelines failed due to permission error. Why does this issue occur and how to resolve it?<br></br>
A: sometimes cache save ho jati ha server pay tou ap ko jo wo path deti ha us may ja kay cache remove kartey hain sudo rm –rf <br></br>
Q8: Kubernetes may aik pod ha ya aik container ha wo crash backoff may phasa hua ha?<br></br>
A: kubectl logs, kubectl describe pods <pod-name>, akser ye error is wajha say hota ha kay humney image ka naam ghalat define kr diya ha..<br></br>
Q9: Difference between Security groups and NACL's?<br></br>
Q10: What is the difference between layer4 and layer 7 load balancer?<br></br>
A: Load balancers distribute incoming traffic across multiple servers, but they operate at different layers of the OSI model, which affects how they make decisions.<br></br>

🔹 Layer 4 Load Balancer (Transport Layer)<br></br>

How it works:<br></br>

Operates at Layer 4 (TCP/UDP).<br></br>

Makes routing decisions based on IP address, port number, and protocol.<br></br>

Does not inspect the actual data (payload) of packets.<br></br>

Key characteristics:<br></br>

Fast and efficient (low latency)<br></br>

Protocol-based routing only<br></br>

No understanding of HTTP/HTTPS content<br></br>

Example use cases:<br></br>

Simple TCP/UDP traffic distribution<br></br>

High-performance applications where speed matters<br></br>

Examples:<br></br>

TCP load balancing in NGINX (stream module)<br></br>

AWS Network Load Balancer (NLB)<br></br>

🔹 Layer 7 Load Balancer (Application Layer)<br></br>

How it works:<br></br>

Operates at Layer 7 (HTTP/HTTPS).<br></br>

Inspects application-level data such as:<br></br>

URL path (/api, /login)<br></br>

HTTP headers<br></br>

Cookies<br></br>

Hostnames<br></br>

Key characteristics:<br></br>

Content-aware routing<br></br>

Supports SSL termination<br></br>

Can perform advanced features like caching, authentication, and rate limiting<br></br>

Slightly higher latency than L4<br></br>

Example use cases:<br></br>

Routing traffic based on URLs or domains<br></br>

Microservices and API gateways<br></br>

Web applications<br></br>

Examples:<br></br>

NGINX, HAProxy<br></br>

AWS Application Load Balancer (ALB)<br></br>

# Round 2<br></br>
Q: Dockerfile likhwai manually<br></br>
Q: DevOps kia hota ha ? Ye kaam tou aik IT wala banda bhi kr sakta ha tou phir devops engineer hi kyu chahiye ? MyAns: server wagera manage karna hota ha InterviewerReply: Acha btao server may kia manage karna hota ha?<br></br>
Q: Linux ka aik tool ha logs dekhney wala btao wo kia ha aur logs kaisey dekhtey ?<br></br>
Q: Apney aik app deploy ki aur 5 min baad us pay 500 internal server error a gya ap kis tarha us ko solve kro gay?<br></br>
Q: Ma google.com hit karta hu step by step btao peechey kia hoga?<br></br>
Q: What is difference between VM and docker? <br></br>
Q: Meri aik file ha 256GB ki you jb ma VM pay ya docker pay use karta hu us nay tou 256 GB hi consume karna ha then why not you choose VM and why you choose docker?<br></br>
Q: aik app deploy ki ha us ka pdf preview show nhi ho rha kaisey set kro ge?<br></br>
Q: I am using Loadbalancer in aws for 4 instances and i want my 20% traffic to go on instance 1, 30% traffic to go on instance 2, 25% traffic to go on instance 3 amd 25% traffic to go on instance 4. how this thing can be achieved?<br></br>
Q: What are ingress services?<br></br>
Q: introduction why are u moving or switching?
Q: diff bw fargate and ec2?
Q: how to check disk space in linux ubuntu?
Q: sonarqube ?
Q: github?
Q: if a pod is stuck in crash error with specific triuble shooting steps?
Q: if a new deployment fails how will u debug?
Q: If we have EC2 them why there's a need of ECS?
Q: What is the abbreviation of NAT gateway?
Q: What happens or what is the expected behaviour when CPU and RAM of server are full? The website deployed on it are working or not?
A: CPU is manage by server/OS kerner so if CPU memory is full. It still runs your already deployed applications because you previously assigned it resources like use 1 CPU etc and if new requesr come then CPU make the processing slow or adds it in a queue but in case of RAM if RAM gets full then all the services crashes because it is not managed by server or OS kernel<br></br>
Q: if we can use ecs for running containers then why do we need ec2 vm for running containers and vice versa?
Q: Pipeline ki stages ma aik aisi koi stage hum bna saktey hain jaha pay koi permission ya approval lein?
Q: What is fartgate?<br></br>
Q: i have two public ec2 instances present in a two different subnets. Now if i want to remove the internet connection of one ec2 instance..What can i do?  I simply remove the internet gateway route from its route table..<br></br>

Q: let suppose we have a 3 tier architecture..so what is my approach i should go for ecs or ec2? Ans: my approach is if i want a fully control on my infra.. i want to manage all the networking each and everything then i should go for ec2 else i should go for ecs... one more take on this is kay if we have a legacy code base and difficult to do its orchestration then we should go for ec2 else we should go for ecs <br></br> but one more question is kay how we can connect ecs with aws database?<br></br>

Q: Aik multistage docker file thi but node as a base image use hui vi thi aur multiple run commands thi..RUN apt-get update, RUN apt-get install -y git, RUN apt-get install -y curl, RUN apt-get install -y vim, RUN npm install, RUN npm run lint, RUN npm run test, RUN npm run build  question ye tha kay dockerfile ko optimze karna ha.?<br></br>
A: saab sa pehle alpine as a base image use karni thi kyu kay wo light weight ha aur multiple run commands ki jagha single run command use karni thi <br></br>
Your Dockerfile can be optimized significantly by:<br></br>

Reducing the number of layers.<br></br>
Using npm ci instead of npm install for reproducible builds.<br></br>
Installing packages in a single RUN command.<br></br>
Removing unnecessary packages (vim, telnet, net-tools) from the final image unless they're absolutely required.<br></br>
Copying only package*.json first to leverage Docker layer caching.<br></br>
Copying only build artifacts to the runtime image instead of the entire application.<br></br>
Here's an optimized version:<br></br>
// Build stage<br></br>
FROM node:20 AS builder<br></br>

WORKDIR /app<br></br>

// Copy dependency files first for better caching<br></br>
COPY package*.json ./<br></br>

// Install dependencies<br></br>
RUN npm ci<br></br>

// Copy source code<br></br>
COPY . .<br></br>

// Install build-only tools if needed<br></br>
RUN apt-get update && \<br></br>
    apt-get install -y --no-install-recommends git curl && \<br></br>
    rm -rf /var/lib/apt/lists/*<br></br>

// Run checks and build<br></br>
RUN npm run lint && \<br></br>
    npm run test && \<br></br>
    npm run build<br></br>


// Runtime stage<br></br>
FROM node:20-slim AS runner<br></br>

WORKDIR /app<br></br>

ENV NODE_ENV=production<br></br>

// Copy package files<br></br>
COPY package*.json ./<br></br>

// Install only production dependencies<br></br>
RUN npm ci --omit=dev && \<br></br>
    npm cache clean --force<br></br>

// Copy build output<br></br>
COPY --from=builder /app/dist ./dist<br></br>

// If your app requires other files (e.g. public, config)<br></br>
// COPY --from=builder /app/public ./public<br></br>

// Install only required runtime utilities<br></br>
RUN apt-get update && \<br></br>
    apt-get install -y --no-install-recommends curl && \<br></br>
    rm -rf /var/lib/apt/lists/*<br></br>

EXPOSE 3000<br></br>

HEALTHCHECK --interval=30s --timeout=5s --start-period=10s --retries=3 \<br></br>
    CMD curl -f http://localhost:3000 || exit 1<br></br>

CMD ["npm", "start"]<br></br>

# Dockerfile Explanation

This document explains each line of the optimized Dockerfile used for building and running a Node.js application.

---

## Complete Dockerfile

```dockerfile
# Build stage
FROM node:20 AS builder

WORKDIR /app

# Copy dependency files first for better caching
COPY package*.json ./

# Install dependencies
RUN npm ci

# Copy source code
COPY . .

# Install build-only tools if needed
RUN apt-get update && \
    apt-get install -y --no-install-recommends git curl && \
    rm -rf /var/lib/apt/lists/*

# Run checks and build
RUN npm run lint && \
    npm run test && \
    npm run build

# Runtime stage
FROM node:20-slim AS runner

WORKDIR /app

ENV NODE_ENV=production

# Copy package files
COPY package*.json ./

# Install only production dependencies
RUN npm ci --omit=dev && \
    npm cache clean --force

# Copy build output
COPY --from=builder /app/dist ./dist

# Install runtime utilities
RUN apt-get update && \
    apt-get install -y --no-install-recommends curl && \
    rm -rf /var/lib/apt/lists/*

EXPOSE 3000

HEALTHCHECK --interval=30s --timeout=5s --start-period=10s --retries=3 \
    CMD curl -f http://localhost:3000 || exit 1

CMD ["npm", "start"]
```

---

# Detailed Explanation

## Build Stage

### `FROM node:20 AS builder`

```dockerfile
FROM node:20 AS builder
```

- Uses the official Node.js version 20 image as the base image.
- `AS builder` names this stage **builder**.
- This stage is responsible for:
  - Installing dependencies
  - Running tests
  - Building the application

This is part of a **multi-stage build**.

---

### `WORKDIR /app`

```dockerfile
WORKDIR /app
```

- Sets `/app` as the working directory inside the container.
- If the directory does not exist, Docker creates it automatically.
- All subsequent commands run relative to this directory.

Equivalent Linux commands:

```bash
mkdir -p /app
cd /app
```

---

### `COPY package*.json ./`

```dockerfile
COPY package*.json ./
```

Copies dependency-related files into the container.

Examples:

```text
package.json
package-lock.json
```

Why copy these files first?

Docker caches layers.

If application source code changes but dependency files remain unchanged, Docker reuses the dependency installation layer, resulting in faster builds.

---

### `RUN npm ci`

```dockerfile
RUN npm ci
```

Installs project dependencies exactly as defined in `package-lock.json`.

Benefits:

- Faster than `npm install`
- Provides reproducible builds
- Ideal for CI/CD pipelines and Docker

---

### `COPY . .`

```dockerfile
COPY . .
```

Copies the entire application source code into the container.

Example:

```text
src/
public/
package.json
```

becomes:

```text
/app/src
/app/public
/app/package.json
```

---

### Install Required Tools

```dockerfile
RUN apt-get update && \
    apt-get install -y --no-install-recommends git curl && \
    rm -rf /var/lib/apt/lists/*
```

This command performs three tasks.

#### 1. Update package index

```bash
apt-get update
```

Downloads the latest package information from Debian repositories.

---

#### 2. Install packages

```bash
apt-get install -y --no-install-recommends git curl
```

Installs:

- `git`
- `curl`

Options used:

| Option | Description |
|---------|-------------|
| `-y` | Automatically answers "yes" |
| `--no-install-recommends` | Avoids installing unnecessary extra packages |

---

#### 3. Remove package cache

```bash
rm -rf /var/lib/apt/lists/*
```

Deletes cached package lists to reduce image size.

---

### Run Linting, Tests, and Build

```dockerfile
RUN npm run lint && \
    npm run test && \
    npm run build
```

Runs the following commands sequentially:

#### Lint

```bash
npm run lint
```

Checks code quality and coding standards.

Examples:

- Missing semicolons
- Unused variables
- Formatting issues

---

#### Tests

```bash
npm run test
```

Runs automated tests using frameworks such as:

- Jest
- Mocha
- Vitest

Build stops if tests fail.

---

#### Build

```bash
npm run build
```

Generates optimized production files.

Examples:

| Framework | Output Directory |
|------------|----------------|
| NestJS | `dist/` |
| React | `build/` |
| Next.js | `.next/` |

---

# Runtime Stage

## `FROM node:20-slim AS runner`

```dockerfile
FROM node:20-slim AS runner
```

Starts a new stage using a smaller Node.js image.

Benefits:

- Smaller image size
- Better security
- Faster deployment

Only this stage becomes the final production image.

---

## `WORKDIR /app`

```dockerfile
WORKDIR /app
```

Sets `/app` as the working directory for the runtime container.

---

## `ENV NODE_ENV=production`

```dockerfile
ENV NODE_ENV=production
```

Creates an environment variable.

Applications can access it using:

```javascript
process.env.NODE_ENV
```

Common uses:

- Enable production optimizations
- Disable debugging features
- Improve performance

---

## `COPY package*.json ./`

```dockerfile
COPY package*.json ./
```

Copies package files into the runtime image because they are required to install production dependencies.

---

## Install Production Dependencies

```dockerfile
RUN npm ci --omit=dev && \
    npm cache clean --force
```

### Install only production packages

```bash
npm ci --omit=dev
```

Installs dependencies listed under:

```json
"dependencies"
```

Excludes packages under:

```json
"devDependencies"
```

Example:

```json
{
  "dependencies": {
    "express": "^5.0.0"
  },
  "devDependencies": {
    "jest": "^30.0.0"
  }
}
```

Only `express` gets installed.

---

### Remove npm cache

```bash
npm cache clean --force
```

Clears npm cache to reduce image size.

---

## Copy Build Artifacts

```dockerfile
COPY --from=builder /app/dist ./dist
```

Copies the compiled application from the `builder` stage.

Syntax:

```dockerfile
COPY --from=<stage-name> <source> <destination>
```

Example:

```dockerfile
COPY --from=builder /app/dist ./dist
```

This ensures that only the built application is included in the final image.

Source code and development tools are excluded.

---

## Install Runtime Utilities

```dockerfile
RUN apt-get update && \
    apt-get install -y --no-install-recommends curl && \
    rm -rf /var/lib/apt/lists/*
```

Installs `curl`, which is required for the health check.

No unnecessary tools are installed.

---

## Expose Application Port

```dockerfile
EXPOSE 3000
```

Documents that the container listens on port `3000`.

> **Note:** `EXPOSE` does not publish the port.

To access the application externally:

```bash
docker run -p 3000:3000 my-app
```

---

## Health Check

```dockerfile
HEALTHCHECK --interval=30s --timeout=5s --start-period=10s --retries=3 \
    CMD curl -f http://localhost:3000 || exit 1
```

Docker periodically checks whether the application is healthy.

### Options

| Option | Description |
|---------|-------------|
| `--interval=30s` | Run check every 30 seconds |
| `--timeout=5s` | Fail if no response within 5 seconds |
| `--start-period=10s` | Wait 10 seconds before first check |
| `--retries=3` | Mark container unhealthy after 3 failures |

Command executed:

```bash
curl -f http://localhost:3000
```

If the command fails:

```bash
exit 1
```

Docker marks the container as **unhealthy**.

---

## Default Startup Command

```dockerfile
CMD ["npm", "start"]
```

Defines the default command executed when the container starts.

Equivalent command:

```bash
npm start
```

When you run:

```bash
docker run my-app
```

Docker automatically executes:

```bash
npm start
```

---

# Multi-Stage Build Workflow

```text
Builder Stage
│
├── Install dependencies
├── Copy source code
├── Lint application
├── Run tests
└── Build application
         │
         ▼
Runner Stage
│
├── Install production dependencies
├── Copy compiled files
├── Configure environment
└── Start application
```

---

# Benefits of This Dockerfile

✅ Smaller image size

✅ Faster builds

✅ Better caching

✅ Improved security

✅ Reduced attack surface

✅ Production-ready container

# Q: why we use this command COPY --from=builder /app/dist ./dist in docker file<br></br>
## Copy Build Artifacts

```dockerfile
COPY --from=builder /app/dist ./dist
```

This is one of the most important instructions in a **multi-stage Docker build**. It copies the compiled application from the **builder stage** to the **final runtime stage**.

---

## General Syntax

```dockerfile
COPY --from=<stage-name> <source-path> <destination-path>
```

| Part | Description |
|-------|-------------|
| `--from=builder` | Specifies the stage from which files should be copied |
| `/app/dist` | Source directory inside the builder stage |
| `./dist` | Destination directory inside the current stage |

---

## Breaking Down the Command

### 1. `--from=builder`

```dockerfile
COPY --from=builder ...
```

Earlier in the Dockerfile, we defined:

```dockerfile
FROM node:20 AS builder
```

Here:

- `node:20` is the base image.
- `builder` is the name assigned to this stage.

Docker creates a temporary image for this stage during the build process.

The `--from=builder` option tells Docker:

> Copy files from the stage named **builder** instead of copying files from the local machine.

Without `--from`, Docker copies files from the build context (your local project directory).

---

### 2. `/app/dist`

This is the **source path** inside the `builder` stage.

After executing:

```bash
npm run build
```

your project inside the builder container might look like this:

```text
/app
├── src/
├── package.json
├── node_modules/
├── tests/
├── .git/
└── dist/
    ├── main.js
    ├── app.js
    └── utils.js
```

The `dist/` directory contains the compiled production-ready application.

For example:

```text
src/main.ts
```

gets compiled into:

```text
dist/main.js
```

The command:

```dockerfile
COPY --from=builder /app/dist
```

tells Docker to copy only the contents of:

```text
/app/dist
```

from the builder stage.

---

### 3. `./dist`

This is the destination path inside the **current stage** (the runtime stage).

Suppose the runtime stage contains:

```dockerfile
FROM node:20-slim AS runner

WORKDIR /app
```

Since the working directory is already set to:

```text
/app
```

the destination:

```dockerfile
./dist
```

actually means:

```text
/app/dist
```

inside the runtime container.

After copying, the runtime container will contain:

```text
/app
└── dist/
    ├── main.js
    ├── app.js
    └── utils.js
```

---

## Why Use Multi-Stage Copy?

Consider the following directory structure inside the builder stage:

```text
/app
├── src/
├── tests/
├── docs/
├── .git/
├── node_modules/
├── coverage/
├── package.json
└── dist/
```

Most of these files are **not required in production**.

Typically, only the compiled application is needed:

```text
dist/
```

By copying only `dist/`, the final image becomes:

- Smaller
- Faster to deploy
- More secure
- Easier to maintain

---

## Without Multi-Stage Builds

A traditional Dockerfile might look like:

```dockerfile
COPY . .
RUN npm install
RUN npm run build
```

The final image would contain:

```text
src/
tests/
.git/
coverage/
node_modules/
dist/
```

This means unnecessary files are included in production.

Example:

```text
Source code
Test files
Git history
Documentation
Coverage reports
```

This can significantly increase the image size.

---

## With Multi-Stage Builds

### Builder Stage

```dockerfile
FROM node:20 AS builder
```

Contains:

```text
src/
tests/
.git/
node_modules/
dist/
```

### Runner Stage

```dockerfile
FROM node:20-slim AS runner
```

Contains only:

```text
production node_modules/
dist/
```

As a result:

✅ Smaller image size

✅ Better security

✅ Faster deployment

✅ Reduced attack surface

---

## Visual Representation

### Builder Stage

```text
+--------------------------------------+
| builder                              |
|--------------------------------------|
| src/                                 |
| tests/                               |
| docs/                                |
| node_modules/                        |
| .git/                                |
| package.json                         |
| dist/                                |
+--------------------------------------+
```

After:

```dockerfile
COPY --from=builder /app/dist ./dist
```

### Runner Stage

```text
+--------------------------------------+
| runner                               |
|--------------------------------------|
| package.json                         |
| production node_modules/             |
| dist/                                |
+--------------------------------------+
```

---

## Example: NestJS Application

Suppose your NestJS project contains:

```text
src/
├── main.ts
├── app.module.ts
└── users/
```

After running:

```bash
npm run build
```

NestJS generates:

```text
dist/
├── main.js
├── app.module.js
└── users/
```

The command:

```dockerfile
COPY --from=builder /app/dist ./dist
```

copies the compiled files into the runtime image.

Finally, the application is started using:

```dockerfile
CMD ["node", "dist/main.js"]
```

Node.js executes the compiled JavaScript files from the `dist/` directory.

---

## Build Output Directories for Different Frameworks

| Framework | Build Output Directory |
|-----------|------------------------|
| NestJS | `dist/` |
| TypeScript | `dist/` |
| Angular | `dist/` |
| Vite | `dist/` |
| React | `build/` |
| Next.js | `.next/` |

Examples:

### React

```dockerfile
COPY --from=builder /app/build ./build
```

### Next.js

```dockerfile
COPY --from=builder /app/.next ./.next
```

---

## Key Takeaway

```dockerfile
COPY --from=builder /app/dist ./dist
```

means:

> Copy the compiled application (`dist/`) from the **builder stage** into the **runtime stage**, so that the final Docker image contains only the files required to run the application.

# Nginx related mcqs questions:<br></br>

# Understanding URI in Nginx `proxy_pass`

## What is a URI?

**URI (Uniform Resource Identifier)** is simply the part of a URL that identifies a specific resource on a server.

In the context of Nginx, you can think of a URI as:

> Everything that comes **after the domain name (host)**.

---

## Example URL

```text
https://example.com/api/users?id=123
```

This URL consists of:

| Component | Value |
|-----------|-------|
| Protocol | `https` |
| Host (Domain) | `example.com` |
| URI | `/api/users?id=123` |

The URI itself can be divided into:

- **Path:** `/api/users`
- **Query String:** `?id=123`

---

## URI in Nginx `proxy_pass`

Understanding whether `proxy_pass` contains a URI is important because Nginx behaves differently depending on it.

---

## Example 1: No URI in `proxy_pass`

```nginx
location /api {
    proxy_pass https://backend;
}
```

### Breakdown

| Part | Value |
|-------|-------|
| Protocol | `https` |
| Host | `backend` |
| URI | ❌ None |

Since no URI is specified, Nginx forwards the original request URI unchanged.

### Client Request

```text
/api/user
```

### Forwarded Request

```text
https://backend/api/user
```

---

## Example 2: URI Present in `proxy_pass`

```nginx
location /api {
    proxy_pass https://backend/;
}
```

### Breakdown

| Part | Value |
|-------|-------|
| Protocol | `https` |
| Host | `backend` |
| URI | `/` |

The `/` after the hostname is considered the URI.

### Client Request

```text
/api/user
```

Nginx removes the matched location prefix:

```text
/api/user
^^^^
```

Remaining part:

```text
/user
```

Then Nginx appends the remaining part to the URI specified in `proxy_pass`.

### Forwarded Request

```text
https://backend/user
```

---

## Example 3: Custom URI in `proxy_pass`

```nginx
location /api {
    proxy_pass https://backend/login/;
}
```

### Breakdown

| Part | Value |
|-------|-------|
| Protocol | `https` |
| Host | `backend` |
| URI | `/login/` |

### Client Request

```text
/api/user
```

Nginx removes `/api` and replaces it with `/login/`.

### Forwarded Request

```text
https://backend/login/user
```

---

## Quick Comparison

### No URI

```nginx
proxy_pass https://backend;
```

Result:

```text
/api       → https://backend/api
/api/user  → https://backend/api/user
```

---

### URI = `/`

```nginx
proxy_pass https://backend/;
```

Result:

```text
/api       → https://backend/
/api/user  → https://backend/user
```

---

### URI = `/login/`

```nginx
proxy_pass https://backend/login/;
```

Result:

```text
/api       → https://backend/login/
/api/user  → https://backend/login/user
```

---

## Visual Representation

### Without URI

```text
Client Request
      |
      v
/api/user
      |
      v
proxy_pass https://backend;
      |
      v
https://backend/api/user
```

---

### With URI

```text
Client Request
      |
      v
/api/user
      |
      v
proxy_pass https://backend/;
      |
      v
https://backend/user
```

---

## Rule to Remember

### ❌ No URI in `proxy_pass`

```nginx
proxy_pass https://backend;
```

> Nginx preserves the complete original request URI.

---

### ✅ URI Present in `proxy_pass`

```nginx
proxy_pass https://backend/;
```

or

```nginx
proxy_pass https://backend/login/;
```

> Nginx replaces the part of the URI matched by the `location` block with the URI specified in `proxy_pass`.

---

## Summary Table

| `proxy_pass` | URI Present? | Request | Forwarded To |
|--------------|-------------|---------|--------------|
| `https://backend` | ❌ No | `/api/user` | `https://backend/api/user` |
| `https://backend/` | ✅ `/` | `/api/user` | `https://backend/user` |
| `https://backend/login/` | ✅ `/login/` | `/api/user` | `https://backend/login/user` |

---

## Key Takeaway

> In Nginx, a **URI** is simply the path that appears after the hostname.
>
> - **No URI in `proxy_pass`** → Original request path is preserved.
> - **URI present in `proxy_pass`** → The matching `location` path is replaced by the URI specified in `proxy_pass`.

# Q: <br></br>
let suppose aik banda ha wo aws kay mumbai waley region ma ha aur buckey use kr rha ha jo kay stockholm ma apri hui ha.. ab rooz wo multiple data post ya fetch karta ha s3 say tou boht ziada cosst ati ha.. kaisey is ko optimize karein gay?<br></br>
# A
answer is s3 endpoint (not cnfr)<br></br>
