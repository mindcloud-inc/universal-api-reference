# Update Subscription with Google Cloud Pub/Sub

Updates a subscription in Google Cloud Pub/Sub.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/:name`
- **Base URL:** `https://pubsub.googleapis.com`
- **Official documentation:** [Update Subscription](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.subscriptions/patch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | Required. Identifier. The name of the subscription. It must have the format `projects/{project}/subscriptions/{subscription}`. |
