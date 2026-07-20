# Validate Schema with Google Cloud Pub/Sub

Validates a schema in Google Cloud Pub/Sub.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/:parent/schemas:validate`
- **Base URL:** `https://pubsub.googleapis.com`
- **Official documentation:** [Validate Schema](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.schemas/validate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parent` | path | `string` | yes | Required. The name of the project in which to validate schemas. Format is `projects/{project-id}`. |
