# Delete Topic with Google Cloud Pub/Sub

Deletes a topic from Google Cloud Pub/Sub.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/:topic`
- **Base URL:** `https://pubsub.googleapis.com`
- **Official documentation:** [Delete Topic](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.topics/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `topic` | path | `string` | yes | Required. Name of the topic to delete. Format is `projects/{project}/topics/{topic}`. |
