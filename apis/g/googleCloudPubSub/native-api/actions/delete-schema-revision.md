# Delete Schema Revision with Google Cloud Pub/Sub

Deletes a schema revision from Google Cloud Pub/Sub.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/:name:deleteRevision`
- **Base URL:** `https://pubsub.googleapis.com`
- **Official documentation:** [Delete Schema Revision](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.schemas/deleteRevision)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | Required. The name of the schema revision to be deleted, with a revision ID explicitly included. Example: `projects/123/schemas/my-schema@c7cfa2a8` |
