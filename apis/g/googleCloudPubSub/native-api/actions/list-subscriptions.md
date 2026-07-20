# List Subscriptions with Google Cloud Pub/Sub

Retrieves subscriptions from Google Cloud Pub/Sub.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/:project/subscriptions`
- **Base URL:** `https://pubsub.googleapis.com`
- **Official documentation:** [List Subscriptions](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.subscriptions/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | path | `string` | yes | Required. The name of the project in which to list subscriptions. Format is `projects/{project-id}`. |
