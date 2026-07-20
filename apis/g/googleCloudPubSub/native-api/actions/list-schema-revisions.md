# List Schema Revisions with Google Cloud Pub/Sub

Retrieves schema revisions from Google Cloud Pub/Sub.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/:name:listRevisions`
- **Base URL:** `https://pubsub.googleapis.com`
- **Official documentation:** [List Schema Revisions](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.schemas/listRevisions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | Required. The name of the schema to list revisions for. |
| `view` | query | `string` | no | The set of Schema fields to return in the response. If not set, returns Schemas with `name` and `type`, but not `definition`. Set to `FULL` to retrieve all fields. |
