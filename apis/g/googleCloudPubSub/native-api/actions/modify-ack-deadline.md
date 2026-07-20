# Modify Ack Deadline with Google Cloud Pub/Sub

Modifies a subscription ack deadline in Google Cloud Pub/Sub.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/:subscription:modifyAckDeadline`
- **Base URL:** `https://pubsub.googleapis.com`
- **Official documentation:** [Modify Ack Deadline](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.subscriptions/modifyAckDeadline)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscription` | path | `string` | yes | Required. The name of the subscription. Format is `projects/{project}/subscriptions/{sub}`. |
