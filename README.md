# Soarsoft

**Developer-first infrastructure and tools to ship SaaS/PaaS/IaaS faster.**  
We build Kotlin-centric backends, Gradle tooling, and self-hosted streaming infrastructure (Slipstream) inside a single, well-structured monorepo.

---

## Mission

Create pragmatic, composable building blocks—CLI, Gradle plugins, Kotlin services, and streaming primitives—that help solo engineers and small teams ship production software quickly without rewiring their stack every project.

---

## What We’re Building

### Slipstream (Alpha)
A self-hosted streaming stack designed for creators and indie platforms.

- **Pipeline:** OBS → RTMP ingest → HLS packaging → web playback
- **Status:** **Alpha** (pre-production). Expect outages and breaking changes.
- **Access:** Limited testing while we harden ingest, auth, metrics, and billing.
- **Watch / Learn More:** https://soarsoft.co/slipstream  
- **Creator handle:** [@iideprived](https://x.com/iideprived)

Planned next:
- Stream key provisioning & rotation
- Basic chat + presence
- Creator analytics (concurrency, watch time)
- CDN integration + recording archival

---

## Tech Stack (current & planned)

- **Language:** Kotlin (JVM), Kotlin Multiplatform (KMP) where it adds leverage  
- **Web/Services:** Ktor (primary), selective Spring Boot interop for legacy/enterprise use
- **UI:** Compose Multiplatform (Web/Desktop) + lightweight HTML/CSS/JS where appropriate
- **Build:** Gradle 8.x, version catalogs (`libs.versions.toml`), custom build-logic
- **Tooling:** Soarsoft CLI (scaffolding, local ops), Soarsoft Scaffold Gradle plugin
- **Data:** PostgreSQL; Redis; S3-compatible object storage; optional Firestore adapters
- **Streaming:** NGINX-RTMP/MediaMTX, FFmpeg, HLS (CMAF in roadmap), Cloudflare for edge
- **Infra:** Docker; GitHub Actions; IaC (Terraform) on the roadmap
- **Observability:** OpenTelemetry; Prometheus/Grafana (planned)
- **Security:** API keys with hashed secrets; role-based access; per-app entitlements (roadmap)

---

## Monorepo (high-level intent)

