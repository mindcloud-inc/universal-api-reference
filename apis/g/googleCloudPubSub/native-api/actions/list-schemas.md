# List Schemas with Google Cloud Pub/Sub

Retrieves schemas from Google Cloud Pub/Sub.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/:parent/schemas`
- **Base URL:** `https://pubsub.googleapis.com`
- **Official documentation:** [List Schemas](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.schemas/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parent` | path | `string` | yes | Required. The name of the project in which to list schemas. Format is `projects/{project-id}`. |
| `view` | query | `string` | no | The set of Schema fields to return in the response. If not set, returns Schemas with `name` and `type`, but not `definition`. Set to `FULL` to retrieve all fields. |
