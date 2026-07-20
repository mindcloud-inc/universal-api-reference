# Get Subscription IAM Policy with Google Cloud Pub/Sub

Retrieves a subscription IAM policy from Google Cloud Pub/Sub.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/:resource:getIamPolicy`
- **Base URL:** `https://pubsub.googleapis.com`
- **Official documentation:** [Get Subscription IAM Policy](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.subscriptions/getIamPolicy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resource` | path | `string` | yes | REQUIRED: The resource for which the policy is being requested. See [Resource names](https://cloud.google.com/apis/design/resource_names) for the appropriate value for this field. |
| `options.requestedPolicyVersion` | query | `number` | no | Optional. The maximum policy version that will be used to format the policy. Valid values are 0, 1, and 3. |
