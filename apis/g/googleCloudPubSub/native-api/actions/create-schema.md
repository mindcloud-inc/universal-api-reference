# Create Schema with Google Cloud Pub/Sub

Creates a schema in Google Cloud Pub/Sub.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/:parent/schemas`
- **Base URL:** `https://pubsub.googleapis.com`
- **Official documentation:** [Create Schema](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.schemas/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parent` | path | `string` | yes | Required. The name of the project in which to create the schema. Format is `projects/{project-id}`. |
| `schemaId` | query | `string` | no | The ID to use for the schema, which will become the final component of the schema's resource name. See https://cloud.google.com/pubsub/docs/pubsub-basics#resource_names for resource name constraints. |
