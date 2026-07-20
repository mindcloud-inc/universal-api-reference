# Detach Subscription with Google Cloud Pub/Sub

Detaches a subscription from its topic in Google Cloud Pub/Sub.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/:subscription:detach`
- **Base URL:** `https://pubsub.googleapis.com`
- **Official documentation:** [Detach Subscription](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.subscriptions/detach)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscription` | path | `string` | yes | Required. The subscription to detach. Format is `projects/{project}/subscriptions/{subscription}`. |
