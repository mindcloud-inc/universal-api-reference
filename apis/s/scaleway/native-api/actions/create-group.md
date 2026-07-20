# Create Group with Scaleway

Creates a new group in Scaleway.

## Endpoint

- **Method:** `POST`
- **Path:** `/iam/v1alpha1/groups`
- **Base URL:** `https://api.scaleway.com`
- **Official documentation:** [Create Group](https://www.scaleway.com/en/developers/api/iam/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `organization_id` | body | `string` | yes |
