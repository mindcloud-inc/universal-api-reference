# NextBrain: Native API Reference

A consolidated summary of NextBrain's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://api.nextbrain.ai/docs
- **OpenAPI specification:** https://api.nextbrain.ai/openapi.json
- **API base URL:** `https://api.nextbrain.ai`

## Authentication

### NextBrain Token

Use a NextBrain access token delivered through the provider's documented user_token header family.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.nextbrain.ai/openapi.json)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Delete Model](actions/delete-model.md) | `DELETE /model/delete_model_token/:model_id` | [docs](https://api.nextbrain.ai/docs) |
| [Get Current User](actions/get-current-user.md) | `POST /login/nextbrain-token` | [docs](https://api.nextbrain.ai/docs) |
| [Get Model Accuracy](actions/get-model-accuracy.md) | `POST /model/acc_token/:model_id` | [docs](https://api.nextbrain.ai/docs) |
| [Get Model Status](actions/get-model-status.md) | `POST /model/status_token/:model_id` | [docs](https://api.nextbrain.ai/docs) |
| [Get Predict Columns](actions/get-predict-columns.md) | `POST /model/predict_columns_token/:model_id` | [docs](https://api.nextbrain.ai/docs) |
| [Import Matrix Data](actions/import-matrix-data.md) | `POST /csv/import_matrix_token` | [docs](https://api.nextbrain.ai/docs) |
| [List Models](actions/list-models.md) | `POST /model/model_ids_token` | [docs](https://api.nextbrain.ai/docs) |
| [Train Model](actions/train-model.md) | `POST /model/train_token` | [docs](https://api.nextbrain.ai/docs) |
