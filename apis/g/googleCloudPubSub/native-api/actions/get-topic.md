# Get Topic with Google Cloud Pub/Sub

Retrieves a topic from Google Cloud Pub/Sub.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/:topic`
- **Base URL:** `https://pubsub.googleapis.com`
- **Official documentation:** [Get Topic](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.topics/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `topic` | path | `string` | yes | Required. The name of the topic to get. Format is `projects/{project}/topics/{topic}`. |
