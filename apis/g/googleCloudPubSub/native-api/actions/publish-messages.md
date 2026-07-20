# Publish Messages with Google Cloud Pub/Sub

Publishes messages to a topic in Google Cloud Pub/Sub.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/:topic:publish`
- **Base URL:** `https://pubsub.googleapis.com`
- **Official documentation:** [Publish Messages](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.topics/publish)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `topic` | path | `string` | yes | Required. The messages in the request will be published on this topic. Format is `projects/{project}/topics/{topic}`. |
