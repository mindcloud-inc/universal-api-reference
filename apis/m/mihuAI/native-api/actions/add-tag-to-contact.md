# Add Tag to Contact with Mihu AI

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/contacts/:uuid/add-tag`
- **Base URL:** `https://{subdomain}.mindhunters.ai`
- **Official documentation:** [Add Tag to Contact](https://developers.mihu.ai/api-reference/contacts/add-tag-to-contact)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `tag_id` | body | `number` | no |
| `uuid` | path | `string` | yes |
