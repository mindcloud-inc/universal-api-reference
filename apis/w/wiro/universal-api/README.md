# <img src="https://images.mindcloud.co/apps/icons/android-icon-192x192_1775138132331.png" alt="Wiro logo" width="28" height="28"> Wiro: Universal API

Run Wiro AI models, inspect model schemas and pricing, manage task lifecycle, and upload files through the Wiro API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/wiro/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://wiro.ai
- **Vendor API docs:** https://wiro.ai/docs/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Explore Models](actions/explore-models.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wiro/latest/actions/explore-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Upload File](actions/upload-file.md) | POST | Uploads a file to Wiro. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Task](actions/cancel-task.md) | PUT | Cancels a queued task in Wiro. |
| [Get Task](actions/get-task.md) | GET | Retrieves the current status and output of a task from Wiro. |
| [Kill Task](actions/kill-task.md) | PUT | Kills a running task in Wiro. |
| [Run Model](actions/run-model.md) | POST | Starts an AI model run in Wiro and returns a task ID. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Explore Models](actions/explore-models.md) | GET | Retrieves curated AI model collections from Wiro. |
| [Get Model Schema](actions/get-model-schema.md) | GET | Retrieves model parameters and details from Wiro. |
| [Search Models](actions/search-models.md) | GET | Finds AI models in Wiro by keyword or category. |

