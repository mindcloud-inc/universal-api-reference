# Get Subscription with Google Cloud Pub/Sub

Retrieves a subscription from Google Cloud Pub/Sub.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/:subscription`
- **Base URL:** `https://pubsub.googleapis.com`
- **Official documentation:** [Get Subscription](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.subscriptions/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscription` | path | `string` | yes | Required. The name of the subscription to get. Format is `projects/{project}/subscriptions/{sub}`. |
