# Create Credential Group with Hyperstack Certificates

## Endpoint

- **Method:** `POST`
- **Path:** `/groups/new`
- **Base URL:** `https://api.thehyperstack.com/v1`
- **Official documentation:** [Create Credential Group](https://thehyperstack.com/docs/api-guide/create-credential-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `badge_template` | body | `string` | no | Badge template key. |
| `blockchain` | body | `boolean` | yes | Enable blockchain anchoring for credentials. |
| `certificate_template` | body | `string` | no | Certificate template key. |
| `description` | body | `string` | yes | Description of the credential group. |
| `does_expire` | body | `boolean` | yes | Whether credentials in this group expire. |
| `group_code` | body | `string` | yes | Human-readable code for the group. |
| `tags` | body | `object` | yes | Tags related to the credential group. |
| `title` | body | `string` | yes | Title of the credential group. |
| `url` | body | `string` | yes | External URL associated with the credential group. |
| `validity` | body | `number` | yes | Validity period in years when does_expire is true. |
