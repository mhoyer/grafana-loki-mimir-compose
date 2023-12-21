# Grafana Stack Docker Examples

Architecture:

```

   ┌── Grafana ──┐
   │             │
   ▼             ▼
  Loki         Mimir
  │  ▲         ▲  │
  │  │         │  │
  │  └─ Agent ─┘  │
  │               │
  │               │
  └───► Minio ◄───┘

```

## Endpoints

Container           | Endpoint
-|-
Grafana             | http://localhost:3000
Grafana-Agent       | http://localhost:12345
Loki endpoint       | http://localhost:3100
Mimir HTTP endpoint | http://localhost:8080
Mimir GRPC endpoint | grpc://localhost:9095
Minio S3 API        | http://localhost:9000
Minio Console       | http://localhost:9001
