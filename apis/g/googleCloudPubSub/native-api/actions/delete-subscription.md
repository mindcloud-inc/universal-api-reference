# Delete Subscription with Google Cloud Pub/Sub

Deletes a subscription from Google Cloud Pub/Sub.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/:subscription`
- **Base URL:** `https://pubsub.googleapis.com`
- **Official documentation:** [Delete Subscription](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.subscriptions/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscription` | path | `string` | yes | Required. The subscription to delete. Format is `projects/{project}/subscriptions/{sub}`. |
