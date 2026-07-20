# Delete SSH Key with Scaleway

Deletes an existing SSH key from Scaleway.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/iam/v1alpha1/ssh-keys/:ssh_key_id`
- **Base URL:** `https://api.scaleway.com`
- **Official documentation:** [Delete SSH Key](https://www.scaleway.com/en/developers/api/iam/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ssh_key_id` | path | `string` | yes |
