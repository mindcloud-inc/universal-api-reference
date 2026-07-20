# Modify Push Config with Google Cloud Pub/Sub

Modifies a subscription push config in Google Cloud Pub/Sub.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/:subscription:modifyPushConfig`
- **Base URL:** `https://pubsub.googleapis.com`
- **Official documentation:** [Modify Push Config](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.subscriptions/modifyPushConfig)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscription` | path | `string` | yes | Required. The name of the subscription. Format is `projects/{project}/subscriptions/{sub}`. |
