# List Snapshots with Google Cloud Pub/Sub

Retrieves snapshots from Google Cloud Pub/Sub.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/:project/snapshots`
- **Base URL:** `https://pubsub.googleapis.com`
- **Official documentation:** [List Snapshots](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.snapshots/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | path | `string` | yes | Required. The name of the project in which to list snapshots. Format is `projects/{project-id}`. |
