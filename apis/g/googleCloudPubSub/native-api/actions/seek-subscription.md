# Seek Subscription with Google Cloud Pub/Sub

Seeks a subscription to a timestamp or snapshot in Google Cloud Pub/Sub.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/:subscription:seek`
- **Base URL:** `https://pubsub.googleapis.com`
- **Official documentation:** [Seek Subscription](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.subscriptions/seek)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscription` | path | `string` | yes | Required. The subscription to affect. |
