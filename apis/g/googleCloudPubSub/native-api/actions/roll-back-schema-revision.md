# Roll Back Schema Revision with Google Cloud Pub/Sub

Rolls back a schema revision in Google Cloud Pub/Sub.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/:name:rollback`
- **Base URL:** `https://pubsub.googleapis.com`
- **Official documentation:** [Roll Back Schema Revision](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.schemas/rollback)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | Required. The schema being rolled back with revision id. |
