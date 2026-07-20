# List Topic Subscriptions with Google Cloud Pub/Sub

Retrieves subscriptions for a topic in Google Cloud Pub/Sub.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/:topic/subscriptions`
- **Base URL:** `https://pubsub.googleapis.com`
- **Official documentation:** [List Topic Subscriptions](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.topics.subscriptions/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `topic` | path | `string` | yes | Required. The name of the topic that subscriptions are attached to. Format is `projects/{project}/topics/{topic}`. |
