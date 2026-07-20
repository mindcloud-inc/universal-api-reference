# Test Snapshot IAM Permissions with Google Cloud Pub/Sub

Tests snapshot IAM permissions in Google Cloud Pub/Sub.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/:resource:testIamPermissions`
- **Base URL:** `https://pubsub.googleapis.com`
- **Official documentation:** [Test Snapshot IAM Permissions](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.snapshots/testIamPermissions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resource` | path | `string` | yes | REQUIRED: The resource for which the policy detail is being requested. See [Resource names](https://cloud.google.com/apis/design/resource_names) for the appropriate value for this field. |
