<h1 align="center">Mukhriddin Khodieff</h1>
<h3 align="center">Senior Software Engineer · Go & Platform Engineer · AI Infrastructure</h3>

<p align="center">
  I design and run high-performance backends in Go, build cloud-native platforms,<br/>
  and deploy bare-metal GPU clusters (NVIDIA HGX B200) for LLM training & inference.
</p>

<p align="center">
  <a href="https://github.com/mukhriddin-dev?tab=followers"><img src="https://img.shields.io/github/followers/mukhriddin-dev?logo=github&style=for-the-badge&color=0e75b6" /></a>
  <img src="https://komarev.com/ghpvc/?username=mukhriddin-dev&label=Profile%20views&color=0e75b6&style=for-the-badge" />
  <a href="https://wakatime.com/@8ec9d743-2300-4556-b0b7-7af353685a76"><img src="https://wakatime.com/badge/user/8ec9d743-2300-4556-b0b7-7af353685a76.svg" /></a>
</p>

---

## ⚡ Core Focus

| Area | What I do |
|---|---|
| **Go Backend** | High-load microservices, gRPC APIs, event-driven systems, low-latency services |
| **Platform / DevOps / SRE** | Kubernetes platforms, GitOps, IaC, observability, zero-downtime delivery |
| **AI Infrastructure** | HGX B200 cluster bring-up, GPU networking, LLM inference & training stacks |
| **Full-stack** | React / Next.js / Vue frontends on top of the platforms I build |

---

## 🐹 Go Engineering

<p>
  <img src="https://skillicons.dev/icons?i=go,postgres,redis,kafka,rabbitmq,mongodb,graphql&perline=10" />
</p>

- **Frameworks & libs:** Gin, Echo, Fiber, Chi, net/http (std), gRPC + Protobuf, Connect-RPC
- **Data:** pgx, sqlc, GORM, Ent, go-redis, MongoDB driver
- **Messaging & streaming:** Kafka (franz-go, sarama), NATS / JetStream, RabbitMQ
- **Architecture:** Clean / Hexagonal architecture, DDD, CQRS, Event Sourcing, Saga, Outbox pattern
- **Concurrency:** goroutines & channels, worker pools, context propagation, rate limiting, backpressure
- **Performance:** pprof, trace, benchmarks, escape analysis, memory/GC tuning
- **Reliability:** circuit breakers, retries with jitter, idempotency, graceful shutdown
- **Testing:** testify, gomock, testcontainers-go, fuzzing, table-driven tests
- **Tooling:** Go modules & workspaces, golangci-lint, Wire / Fx (DI), Cobra CLIs, Kubernetes operators (controller-runtime, Kubebuilder)

---

## ☸️ DevOps · Platform Engineering · SRE

<p>
  <img src="https://skillicons.dev/icons?i=docker,kubernetes,terraform,ansible,linux,ubuntu,nginx,githubactions,gitlab,prometheus,grafana,aws,gcp,cloudflare&perline=14" />
</p>

- **Containers & orchestration:** Docker, Kubernetes (kubeadm, k3s, EKS/GKE), Helm, Kustomize
- **GitOps & CI/CD:** Argo CD, Flux, GitHub Actions, GitLab CI, Argo Workflows / Rollouts (canary, blue-green)
- **Infrastructure as Code:** Terraform / OpenTofu, Ansible, Packer, cloud-init
- **Networking:** Cilium (eBPF), Calico, Istio / Linkerd, Ingress-NGINX, Traefik, MetalLB, HAProxy, Envoy
- **Observability:** Prometheus, Grafana, Loki, Tempo, OpenTelemetry, Alertmanager, VictoriaMetrics
- **Storage:** Ceph / Rook, Longhorn, MinIO (S3), NFS, local NVMe
- **Security:** Vault, cert-manager, external-secrets, Trivy, Kyverno / OPA, RBAC, network policies, SSO (Keycloak)
- **SRE practices:** SLO/SLI, incident response, postmortems, capacity planning, chaos testing
- **Linux:** kernel & sysctl tuning, systemd, networking (iproute2, bonding, VLANs), bash automation

---

## 🔥 AI Infrastructure — NVIDIA HGX B200 Clusters

End-to-end bring-up of bare-metal GPU servers: from rack to running LLM endpoints.

**Hardware & bring-up**
- NVIDIA HGX B200 (8× Blackwell GPU, 192 GB HBM3e each, 5th-gen NVLink / NVSwitch)
- Rack planning: power (high-density PDUs, ~14 kW+ per node), cooling (air / direct liquid cooling), cabling
- BMC / IPMI / Redfish, BIOS & firmware updates, PXE / MAAS bare-metal provisioning
- Burn-in & validation: DCGM diagnostics, `nvidia-smi`, NCCL tests, HPL, GPU stress tests

**GPU networking**
- InfiniBand NDR 400G & RoCEv2 (Spectrum-X), NVIDIA ConnectX-7 / BlueField-3 DPU
- Rail-optimized fat-tree topology, UFM, Subnet Manager, GPUDirect RDMA & GPUDirect Storage
- NCCL tuning for multi-node all-reduce performance

**Software stack**
- NVIDIA drivers, CUDA 12.x, Fabric Manager, NVIDIA Container Toolkit
- Kubernetes GPU Operator, Network Operator, MIG partitioning, time-slicing
- Scheduling: Slurm (Pyxis / Enroot), Kueue, Volcano, Run:ai concepts
- Monitoring: DCGM Exporter → Prometheus / Grafana (temps, power, ECC, XID errors, NVLink health)
- High-performance storage: WEKA / VAST / Lustre concepts, NVMe-oF

**LLM serving & training**
- Inference: vLLM, SGLang, TensorRT-LLM, NVIDIA Triton, NVIDIA NIM, llama.cpp, Ollama
- Optimizations: FP8 / FP4 quantization, tensor & pipeline parallelism, continuous batching, KV-cache tuning, speculative decoding
- Distributed training: PyTorch DDP / FSDP, DeepSpeed, Megatron-LM, LoRA / QLoRA fine-tuning
- MLOps: Ray, KServe, Kubeflow, MLflow, LiteLLM gateway (OpenAI-compatible APIs)

---

## 🤖 AI / LLM Application Engineering

- LLM APIs: Anthropic Claude, OpenAI, Gemini, open-weight models (Llama, Qwen, DeepSeek, Mistral)
- RAG pipelines, embeddings, hybrid search, reranking
- Vector DBs: pgvector, Qdrant, Milvus, Weaviate
- AI Agents, tool calling, **MCP (Model Context Protocol)** servers in Go & TypeScript
- LangChain, LangGraph, LlamaIndex, Vercel AI SDK
- Evaluation & observability: Langfuse, LangSmith, OpenTelemetry for LLMs

---

<details>
  <summary><b>🎨 Frontend</b></summary>

<br/>
<img src="https://skillicons.dev/icons?i=ts,js,react,nextjs,vue,nuxtjs,tailwind,sass,vite,jest,vitest&perline=12" />

- TypeScript, React 19, Next.js 15 (App Router, RSC), Vue 3, Nuxt 3
- TanStack Query / Router, Redux Toolkit, Zustand, GraphQL (Apollo)
- TailwindCSS v4, shadcn/ui, Radix, MUI, Ant Design
- Testing: Vitest, Jest, React Testing Library, Playwright, Cypress

</details>

<details>
  <summary><b>🧩 Other Backend</b></summary>

<br/>
<img src="https://skillicons.dev/icons?i=nodejs,nestjs,bun,php,laravel,mysql&perline=10" />

- Node.js, NestJS, Express, Hono, Bun
- PHP 8.3+, Laravel 12, Yii2
- MySQL, Oracle, PostgreSQL, MongoDB
- Prisma, Drizzle ORM

</details>

<details>
  <summary><b>📱 Mobile</b></summary>

<br/>
<img src="https://skillicons.dev/icons?i=react,swift,flutter&perline=5" />

- React Native, Expo
- Swift, SwiftUI
- Ionic

</details>

---

## 📊 GitHub Stats

<p align="center">
  <img height="170" src="https://github-readme-stats.vercel.app/api?username=mukhriddin-dev&show_icons=true&theme=tokyonight&hide_border=true&count_private=true" />
  <img height="170" src="https://github-readme-stats.vercel.app/api/top-langs/?username=mukhriddin-dev&layout=compact&theme=tokyonight&hide_border=true" />
</p>

<p align="center">
  <img src="https://github-profile-trophy.vercel.app/?username=mukhriddin-dev&theme=tokyonight&no-frame=true&row=1&column=7" />
</p>
