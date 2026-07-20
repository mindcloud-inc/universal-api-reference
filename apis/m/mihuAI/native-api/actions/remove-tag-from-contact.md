# Remove Tag from Contact with Mihu AI

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/contacts/:uuid/remove-tag`
- **Base URL:** `https://{subdomain}.mindhunters.ai`
- **Official documentation:** [Remove Tag from Contact](https://developers.mihu.ai/api-reference/contacts/remove-tag-from-contact)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `tag_id` | body | `number` | no |
| `uuid` | path | `string` | yes |
