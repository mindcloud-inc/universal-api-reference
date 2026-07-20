# Create Subscription with Google Cloud Pub/Sub

Creates a subscription in Google Cloud Pub/Sub.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/:name`
- **Base URL:** `https://pubsub.googleapis.com`
- **Official documentation:** [Create Subscription](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.subscriptions/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | Required. Identifier. The name of the subscription. It must have the format `projects/{project}/subscriptions/{subscription}`. |
