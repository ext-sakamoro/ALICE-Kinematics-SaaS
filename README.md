# ALICE-Kinematics SaaS

Human motion intent compression API

## License

AGPL-3.0

## Architecture

```
Frontend :3000  -->  API Gateway :8080  -->  Core Engine :8081
```

| Layer | Port | Technology |
|-------|------|-----------|
| Frontend | 3000 | Next.js 14, Tailwind CSS |
| API Gateway | 8080 | Rust, Axum |
| Core Engine | 8081 | Rust, Axum, ALICE-Kinematics |

## Endpoints

| Method | Path | Description |
|--------|------|-------------|
| `POST /api/v1/compress` | モーションデータ圧縮 |
| `POST /api/v1/decompress` | モーションデータ復元 |
| `POST /api/v1/intent` | 動作意図抽出 |
| `GET`  | `/health` | ヘルスチェック |

## Quick Start

```bash
cd services/core-engine
cargo run --release
curl http://localhost:8081/health
```

## Author

Moroya Sakamoto
