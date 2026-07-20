# Get logs queue with Appwrite

Retrieves Appwrite logs queue metrics.

## Endpoint

- **Method:** `GET`
- **Path:** `/health/queue/logs`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Get logs queue](https://appwrite.io/docs/references/cloud/server-rest/health)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `threshold` | query | `number` | no | Queue size threshold. When hit (equal or higher), endpoint returns server error. Default value is 5000. |
