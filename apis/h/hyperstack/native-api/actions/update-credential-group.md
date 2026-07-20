# Update Credential Group with Hyperstack Certificates

## Endpoint

- **Method:** `POST`
- **Path:** `/group/update/:group_key`
- **Base URL:** `https://api.thehyperstack.com/v1`
- **Official documentation:** [Update Credential Group](https://thehyperstack.com/docs/api-guide/update-credential-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `badge_template` | body | `string` | no | New badge template key. |
| `blockchain` | body | `boolean` | no | Enable blockchain anchoring for credentials in this group. |
| `certificate_template` | body | `string` | no | New certificate template key. |
| `description` | body | `string` | no | Updated credential group description HTML. |
| `group_code` | body | `string` | no | Updated human-readable code for the group. |
| `group_key` | path | `string` | yes | Credential group key to update. |
| `tags` | body | `object` | no | Updated tags for the credential group. |
| `title` | body | `string` | no | Updated credential group title. |
| `url` | body | `string` | no | Updated credential group website URL. |
| `does_expire` | body | `boolean` | yes | Whether credentials in the group expire. |
| `validity` | body | `number` | yes | Validity duration configured for the group. |
