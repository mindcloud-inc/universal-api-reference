# Delete Schema with Google Cloud Pub/Sub

Deletes a schema from Google Cloud Pub/Sub.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/:name`
- **Base URL:** `https://pubsub.googleapis.com`
- **Official documentation:** [Delete Schema](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.schemas/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | Required. Name of the schema to delete. Format is `projects/{project}/schemas/{schema}`. |
