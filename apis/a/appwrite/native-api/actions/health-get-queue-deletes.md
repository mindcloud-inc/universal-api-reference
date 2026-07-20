# Get deletes queue with Appwrite

Retrieves Appwrite deletes queue metrics.

## Endpoint

- **Method:** `GET`
- **Path:** `/health/queue/deletes`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Get deletes queue](https://appwrite.io/docs/references/cloud/server-rest/health)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `threshold` | query | `number` | no | Queue size threshold. When hit (equal or higher), endpoint returns server error. Default value is 5000. |
