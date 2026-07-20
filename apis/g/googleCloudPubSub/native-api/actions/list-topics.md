# List Topics with Google Cloud Pub/Sub

Retrieves topics from Google Cloud Pub/Sub.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/:project/topics`
- **Base URL:** `https://pubsub.googleapis.com`
- **Official documentation:** [List Topics](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.topics/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | path | `string` | yes | Required. The name of the project in which to list topics. Format is `projects/{project-id}`. |
