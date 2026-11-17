# Aeroplane — Feature Suggestions

> Generated after merging `origin/main` (includes rollback, Vercel import, functions, TanStack Start, etc.)

## Status Legend

- [ ] — Not yet implemented
- [x] — Already exists in the codebase

---

## 🚀 Deployment & Build Experience

- [ ] **Deployment rollback** — One-click revert to a previous successful deployment, reusing the old image tag
- [ ] **Deployment previews / ephemeral environments** — Spin up a temporary service instance from a PR branch with a unique URL
- [ ] **Health check configuration** — Let users define health check endpoints, grace periods, and failure thresholds per service
- [ ] **Deployment webhooks** — Outgoing webhooks on deploy start/finish/fail (for Slack, Discord, etc.)
- [ ] **Multi-stage Docker build cache** — Better cache reuse across builds for faster deploys
- [ ] **Rolling updates with canary traffic splitting** — Gradually shift traffic to new containers
- [x] **Service functions / serverless** — Write and deploy serverless functions directly from the dashboard
- [x] **AI-assisted deployment failure analysis** — Get explanations for why a deployment failed

## 🗄️ Databases

- [ ] **MySQL / MariaDB support** — Only PostgreSQL, Redis, and MongoDB are currently supported
- [ ] **Database connection pooling** — PgBouncer-style pooling for Postgres services
- [ ] **Database cloning** — Clone a production DB into a new service for testing
- [ ] **Automated schema migrations** — Run migration scripts as part of the deploy pipeline
- [ ] **Read replicas** — Spin up read-only replicas of Postgres services
- [x] **PostgreSQL logical replication** — Set up logical replication between databases
- [x] **Database browsing & SQL console** — Browse tables, run queries, edit data
- [x] **Automated backups** — Daily, weekly, monthly backups to local or R2 storage
- [x] **Database data import** — Import data from dumps

## 🔐 Security & Access Control

- [ ] **SSO / OAuth login** — Sign in with GitHub, Google, or other OAuth providers (currently only email/password)
- [ ] **Team & multi-user permissions** — Invite team members with granular roles (admin, developer, viewer)
- [ ] **Audit log** — Track who did what (deployments, env changes, config edits)
- [ ] **IP allowlisting** — Restrict dashboard access to specific IP ranges
- [ ] **2FA / TOTP** — Two-factor authentication for dashboard users
- [x] **API keys with scoped access** — Create read-only or read/write keys per project or all projects
- [x] **Rate limiting** — Protect API endpoints from abuse

## 🛠 Infrastructure & Operations

- [ ] **Auto-scaling** — Horizontal scaling rules based on CPU/memory thresholds
- [ ] **Service metrics dashboard** — CPU, memory, request rate, response time graphs per service (Prometheus + Grafana integration, or a lightweight built-in solution)
- [ ] **Alerting & notifications** — Email/Slack/Discord alerts when deployments fail, disks fill up, services go down
- [ ] **Backup to any S3-compatible storage** — Already uses R2; extend to Backblaze, MinIO, AWS S3, etc.
- [ ] **Scheduled tasks / cron jobs** — Run one-off or recurring containers for maintenance tasks
- [ ] **Service auto-restart policies** — Configure restart on failure, memory limits, stop grace periods
- [x] **System monitoring** — Real-time CPU, memory, disk, Docker, network and block I/O metrics
- [x] **System updates** — Git-pull and restart the control plane from the dashboard
- [x] **System maintenance** — Clean up old deployments, logs, and cached data

## 🌐 Networking & Domains

- [ ] **Load balancer mode** — Distribute traffic across multiple containers of the same service
- [ ] **Internal service discovery** — Services can reach each other by name inside the runtime network
- [ ] **DDoS protection / rate limiting** — Per-service rate limiting via Caddy
- [ ] **WebSocket support indicators** — Better visibility into WebSocket-capable services
- [x] **Wildcard root domains** — Auto-generate `*.yourdomain.com` hostnames for services
- [x] **Custom domains** — Attach custom domains with automatic SSL via Caddy
- [x] **DNS provider integration** — Programmatically set DNS records (e.g., for domain verification)

## 🧩 Integrations

- [ ] **GitLab / Bitbucket / Gitea support** — Connect repos from other Git providers
- [ ] **GitHub Actions integration** — Trigger deployments from actions, or report deploy status back
- [ ] **Docker Hub / GHCR registry support** — Deploy from pre-built images on any registry
- [ ] **Terraform / Pulumi provider** — Infrastructure-as-code for managing Aeroplane projects
- [ ] **Kubernetes export** — Generate Kubernetes manifests from a service configuration
- [x] **GitHub App (one-click connect)** — OAuth-based GitHub repo connection
- [x] **Vercel project import** — Migrate projects from Vercel with environment variables and configuration
- [x] **Railway project import** — Import projects from Railway

## 📊 Dashboard & UX

- [ ] **Mobile-responsive dashboard** — Full mobile support for the management UI
- [ ] **Real-time terminal in browser** — SSH-like terminal into running containers from the dashboard
- [ ] **Dark mode toggle** — Already has some theme support; make it user-switchable
- [ ] **Service template library** — One-click deploy popular stacks (Next.js, Django, Rails, Laravel, etc.)
- [ ] **Cost tracking** — Estimate VPS resource usage per project/service
- [x] **Confirmation dialogs** — Confirm before destructive actions (deletion, removal)
- [x] **Deployment logs streaming** — Real-time log output during builds and deployments

## 🔧 Platform Improvements

- [ ] **Plugin system** — Hook into deploy/build lifecycle with custom scripts
- [ ] **Multi-node / cluster support** — Deploy services across multiple VPS nodes
- [ ] **Blue-green deployments** — Full blue-green strategy with traffic switch
- [ ] **Self-hosted runner** — Instead of building on the control plane, delegate builds to remote runners
- [x] **TanStack Start runtime** — Support for TanStack Start server-side rendering
- [x] **Zero-downtime container swaps** — Seamless container replacement during deployment

---

*Last updated: after merging origin/main (includes rollback, Vercel import, functions, TanStack Start, rate limiting, container cleanup, and more).*