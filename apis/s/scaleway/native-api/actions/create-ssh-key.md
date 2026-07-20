# Create SSH Key with Scaleway

Creates a new SSH key in Scaleway.

## Endpoint

- **Method:** `POST`
- **Path:** `/iam/v1alpha1/ssh-keys`
- **Base URL:** `https://api.scaleway.com`
- **Official documentation:** [Create SSH Key](https://www.scaleway.com/en/developers/api/iam/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `public_key` | body | `string` | yes |
| `project_id` | body | `string` | yes |
