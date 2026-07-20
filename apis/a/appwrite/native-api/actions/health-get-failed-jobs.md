# Get number of failed queue jobs with Appwrite

Retrieves the number of failed Appwrite queue jobs.

## Endpoint

- **Method:** `GET`
- **Path:** `/health/queue/failed/{name}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Get number of failed queue jobs](https://appwrite.io/docs/references/cloud/server-rest/health)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | The name of the queue |
| `threshold` | query | `number` | no | Queue size threshold. When hit (equal or higher), endpoint returns server error. Default value is 5000. |
