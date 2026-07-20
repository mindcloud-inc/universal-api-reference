# Update SSH Key with Scaleway

Updates an existing SSH key in Scaleway.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/iam/v1alpha1/ssh-keys/:ssh_key_id`
- **Base URL:** `https://api.scaleway.com`
- **Official documentation:** [Update SSH Key](https://www.scaleway.com/en/developers/api/iam/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ssh_key_id` | path | `string` | yes |
| `name` | body | `string` | no |
| `disabled` | body | `boolean` | no |
