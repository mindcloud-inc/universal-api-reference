# Set Subscription IAM Policy with Google Cloud Pub/Sub

Sets a subscription IAM policy in Google Cloud Pub/Sub.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/:resource:setIamPolicy`
- **Base URL:** `https://pubsub.googleapis.com`
- **Official documentation:** [Set Subscription IAM Policy](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.subscriptions/setIamPolicy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resource` | path | `string` | yes | REQUIRED: The resource for which the policy is being specified. See [Resource names](https://cloud.google.com/apis/design/resource_names) for the appropriate value for this field. |
