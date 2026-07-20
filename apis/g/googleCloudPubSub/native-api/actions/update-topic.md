# Update Topic with Google Cloud Pub/Sub

Updates a topic in Google Cloud Pub/Sub.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/:name`
- **Base URL:** `https://pubsub.googleapis.com`
- **Official documentation:** [Update Topic](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.topics/patch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | Required. Identifier. The name of the topic. It must have the format `projects/{project}/topics/{topic}`. |
