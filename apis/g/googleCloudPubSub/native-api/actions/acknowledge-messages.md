# Acknowledge Messages with Google Cloud Pub/Sub

Acknowledges subscription messages in Google Cloud Pub/Sub.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/:subscription:acknowledge`
- **Base URL:** `https://pubsub.googleapis.com`
- **Official documentation:** [Acknowledge Messages](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.subscriptions/acknowledge)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscription` | path | `string` | yes | Required. The subscription whose message is being acknowledged. Format is `projects/{project}/subscriptions/{sub}`. |
