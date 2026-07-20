# Create Topic with Google Cloud Pub/Sub

Creates a topic in Google Cloud Pub/Sub.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/:name`
- **Base URL:** `https://pubsub.googleapis.com`
- **Official documentation:** [Create Topic](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.topics/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | Required. Identifier. The name of the topic. It must have the format `projects/{project}/topics/{topic}`. |
