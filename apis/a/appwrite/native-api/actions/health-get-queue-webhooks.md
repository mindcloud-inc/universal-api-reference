# Get webhooks queue with Appwrite

Retrieves Appwrite webhooks queue metrics.

## Endpoint

- **Method:** `GET`
- **Path:** `/health/queue/webhooks`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Get webhooks queue](https://appwrite.io/docs/references/cloud/server-rest/health)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `threshold` | query | `number` | no | Queue size threshold. When hit (equal or higher), endpoint returns server error. Default value is 5000. |
