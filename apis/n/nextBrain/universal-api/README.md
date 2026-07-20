# <img src="https://images.mindcloud.co/apps/icons/next-brain_1775493651734.png" alt="NextBrain logo" width="28" height="28"> NextBrain: Universal API

Connect NextBrain so you can validate your workspace token and work with the provider's documented app and integration surfaces from MindCloud.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/nextBrain/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://nextbrain.ai/
- **Vendor API docs:** https://api.nextbrain.ai/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Models](actions/list-models.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nextBrain/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Datasets

| Action | Method | Description |
| --- | --- | --- |
| [Import Matrix Data](actions/import-matrix-data.md) | POST | Imports matrix data into a NextBrain dataset. |

### Models

| Action | Method | Description |
| --- | --- | --- |
| [Delete Model](actions/delete-model.md) | DELETE | Deletes an existing model from NextBrain. |
| [Get Model Accuracy](actions/get-model-accuracy.md) | GET | Retrieves model accuracy metrics from NextBrain. |
| [Get Model Status](actions/get-model-status.md) | GET | Retrieves a model status from NextBrain. |
| [Get Predict Columns](actions/get-predict-columns.md) | GET | Retrieves prediction columns for a NextBrain model. |
| [List Models](actions/list-models.md) | GET | Retrieves available model IDs from NextBrain. |
| [Train Model](actions/train-model.md) | PUT | Starts training a model in NextBrain. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from NextBrain. |

