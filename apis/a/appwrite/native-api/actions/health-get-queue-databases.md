# Get databases queue with Appwrite

Retrieves Appwrite databases queue metrics.

## Endpoint

- **Method:** `GET`
- **Path:** `/health/queue/databases`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Get databases queue](https://appwrite.io/docs/references/cloud/server-rest/health)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Queue name for which to check the queue size |
| `threshold` | query | `number` | no | Queue size threshold. When hit (equal or higher), endpoint returns server error. Default value is 5000. |
