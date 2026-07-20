# Update Group with Scaleway

Updates an existing group in Scaleway.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/iam/v1alpha1/groups/:group_id`
- **Base URL:** `https://api.scaleway.com`
- **Official documentation:** [Update Group](https://www.scaleway.com/en/developers/api/iam/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `group_id` | path | `string` | yes |
| `name` | body | `string` | no |
