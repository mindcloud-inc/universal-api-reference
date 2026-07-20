# Pull Messages with Google Cloud Pub/Sub

Pulls messages from Google Cloud Pub/Sub.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/:subscription:pull`
- **Base URL:** `https://pubsub.googleapis.com`
- **Official documentation:** [Pull Messages](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.subscriptions/pull)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscription` | path | `string` | yes | Required. The subscription from which messages should be pulled. Format is `projects/{project}/subscriptions/{sub}`. |
