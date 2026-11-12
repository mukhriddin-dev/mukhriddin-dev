<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=26&duration=3000&pause=1200&color=00ADD8&center=true&vCenter=true&width=700&height=60&lines=Mukhriddin+Khodieff;Go+%C2%B7+Platform+%C2%B7+AI+Infra;I+build+things+that+don't+fall+over." />

<sub>Senior Software Engineer — backends in Go, clusters on bare metal, GPUs that actually train.</sub>

<br/><br/>

<a href="https://github.com/mukhriddin-dev?tab=followers"><img src="https://img.shields.io/github/followers/mukhriddin-dev?logo=github&style=flat-square&color=00ADD8&labelColor=0d1117" /></a>
<img src="https://komarev.com/ghpvc/?username=mukhriddin-dev&label=views&color=00ADD8&style=flat-square&labelColor=0d1117" />
<a href="https://wakatime.com/@8ec9d743-2300-4556-b0b7-7af353685a76"><img src="https://wakatime.com/badge/user/8ec9d743-2300-4556-b0b7-7af353685a76.svg?style=flat-square" /></a>

</div>

<br/>

```go
package main

import "fmt"

type Engineer struct {
	Name     string
	Lang     string   // the one I reach for first
	Runs     []string // what I keep alive in production
	Trains   string   // what I put the GPUs to work on
	Believes []string
}

func main() {
	me := Engineer{
		Name: "Mukhriddin Khodieff",
		Lang: "Go",
		Runs: []string{"Kubernetes", "PostgreSQL", "Kafka", "NVIDIA HGX B200"},
		Trains: "LLMs, and the infra underneath them",
		Believes: []string{
			"boring technology, sharp tools",
			"if it isn't observable, it isn't done",
			"a deploy should be a non-event",
		},
	}

	fmt.Printf("%+v\n", me)
	// go run . → hire me, or just say hi
}
```

<br/>

## `01` · Go is home

> Small binaries. Explicit errors. No magic. Everything else is a guest.

<p>
  <img src="https://skillicons.dev/icons?i=go,postgres,redis,kafka,rabbitmq,mongodb,graphql,grpc&perline=8" />
</p>

|  |  |
|---|---|
| **Servers** | `net/http` · chi · Echo · Gin · Fiber · gRPC + Protobuf · Connect-RPC · SSE / WebSockets |
| **Data** | `pgx` · `sqlc` · goose / Atlas migrations · GORM · Ent · go-redis · Mongo driver |
| **Messaging** | Kafka (franz-go, sarama) · NATS JetStream · RabbitMQ · Outbox + idempotent consumers |
| **Design** | Clean / Hexagonal · DDD · CQRS · Event Sourcing · Saga · RBAC & multi-tenant scoping |
| **Concurrency** | worker pools · `errgroup` · context everywhere · backpressure · rate limiting · graceful shutdown |
| **Resilience** | circuit breakers · retry + jitter · timeouts by default · dead-letter queues |
| **Performance** | `pprof` · `trace` · benchmarks · escape analysis · GC & memory tuning |
| **Quality** | table-driven tests · testify · gomock · testcontainers-go · fuzzing · golangci-lint |
| **Tooling** | Cobra CLIs · Wire / Fx · Go workspaces · Kubernetes operators (controller-runtime, Kubebuilder) · MCP servers in Go |

<br/>

## `02` · Platform & SRE

```text
git push ─▶ CI ─▶ image ─▶ Argo CD ─▶ Kubernetes ─▶ metrics · logs · traces ─▶ sleep
```

<p>
  <img src="https://skillicons.dev/icons?i=docker,kubernetes,terraform,ansible,linux,nginx,githubactions,gitlab,prometheus,grafana,aws,gcp,cloudflare&perline=13" />
</p>

- **Orchestration** — Kubernetes (kubeadm, k3s, EKS/GKE), Helm, Kustomize, Argo CD / Flux, Argo Rollouts (canary, blue-green)
- **IaC** — Terraform / OpenTofu, Ansible, Packer, cloud-init
- **Network** — Cilium (eBPF), Istio / Linkerd, Envoy, HAProxy, MetalLB, Ingress-NGINX / Traefik
- **Observability** — Prometheus, Grafana, Loki, Tempo, OpenTelemetry, VictoriaMetrics, Alertmanager
- **Security** — Vault, cert-manager, external-secrets, Trivy, Kyverno / OPA, Keycloak, network policies
- **Practice** — SLO/SLI, incident response, blameless postmortems, capacity planning, chaos testing
- **Linux** — sysctl & kernel tuning, systemd, bonding / VLANs, fail2ban & SSH hardening, bash

<br/>

## `03` · Bare-metal GPUs — NVIDIA HGX B200

From rack to running LLM endpoint.

```text
 8× Blackwell GPU ── NVLink 5 / NVSwitch ── 1.5 TB HBM3e per node
        │
 ConnectX-7 / BlueField-3 ── InfiniBand NDR 400G · RoCEv2 ── rail-optimized fat-tree
        │
 Kubernetes + GPU Operator ── Slurm / Kueue / Volcano ── vLLM · SGLang · TensorRT-LLM
```

| Layer | Stack |
|---|---|
| **Bring-up** | rack planning (power, air / liquid cooling, cabling) · BMC / IPMI / Redfish · PXE / MAAS · firmware |
| **Validation** | DCGM diagnostics · NCCL tests · HPL · burn-in & GPU stress |
| **Fabric** | UFM · Subnet Manager · GPUDirect RDMA / Storage · NCCL tuning for multi-node all-reduce |
| **Runtime** | drivers · CUDA 12.x · Fabric Manager · Container Toolkit · MIG · time-slicing |
| **Serving** | vLLM · SGLang · TensorRT-LLM · Triton · NIM · llama.cpp · Ollama · FP8 / FP4 · KV-cache · speculative decoding |
| **Training** | PyTorch DDP / FSDP · DeepSpeed · Megatron-LM · LoRA / QLoRA |
| **MLOps** | Ray · KServe · Kubeflow · MLflow · LiteLLM gateway |
| **Telemetry** | DCGM Exporter → Prometheus / Grafana — temps, power, ECC, XID, NVLink health |

<br/>

## `04` · LLM apps & agents

Claude · OpenAI · Gemini · Llama · Qwen · DeepSeek · Mistral — RAG with hybrid search + reranking (pgvector, Qdrant, Milvus), tool-calling agents, and **MCP servers** in Go & TypeScript. LangGraph · LlamaIndex · Vercel AI SDK · Langfuse · LangSmith.

<br/>

<details>
<summary><b>Everything else I touch</b></summary>

<br/>

**Frontend** — TypeScript · React 19 · Next.js 15 · Vue 3 · Nuxt 3 · TanStack · Tailwind v4 · shadcn/ui · Vitest · Playwright
<br/><img src="https://skillicons.dev/icons?i=ts,react,nextjs,vue,nuxtjs,tailwind,vite&perline=10" />

**Other backends** — Node.js · NestJS · Hono · Bun · PHP 8.3 / Laravel 12 · Prisma · Drizzle · MySQL · Oracle
<br/><img src="https://skillicons.dev/icons?i=nodejs,nestjs,bun,php,laravel,mysql&perline=10" />

**Mobile** — React Native · Expo · Swift / SwiftUI · Ionic

</details>

<br/>

<div align="center">

<img height="150" src="https://github-readme-stats.vercel.app/api?username=mukhriddin-dev&show_icons=true&theme=transparent&title_color=00ADD8&icon_color=00ADD8&text_color=8b949e&hide_border=true&count_private=true&hide_title=true" />
<img height="150" src="https://github-readme-stats.vercel.app/api/top-langs/?username=mukhriddin-dev&layout=compact&theme=transparent&title_color=00ADD8&text_color=8b949e&hide_border=true" />

<br/>

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=14&duration=4000&pause=1500&color=8b949e&center=true&vCenter=true&width=500&height=30&lines=func+(me+*Engineer)+Ship()+error+%7B+return+nil+%7D" />

</div>
