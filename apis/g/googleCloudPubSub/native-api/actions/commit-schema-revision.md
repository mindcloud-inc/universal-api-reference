# Commit Schema Revision with Google Cloud Pub/Sub

Commits a new schema revision in Google Cloud Pub/Sub.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/:name:commit`
- **Base URL:** `https://pubsub.googleapis.com`
- **Official documentation:** [Commit Schema Revision](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.schemas/commit)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | Required. The name of the schema we are revising. Format is `projects/{project}/schemas/{schema}`. |
