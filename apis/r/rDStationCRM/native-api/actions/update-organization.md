# Update Organization with RD Station CRM

Updates an existing organization in RD Station CRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/organizations/:id`
- **Base URL:** `https://api.rd.services/crm/v2`
- **Official documentation:** [Update Organization](https://developers.rdstation.com/reference/crm-v2-update-organization)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | yes | Organization payload documented in endpoint reference. |
| `data.address` | body | `object` | no | Endereço da empresa. |
| `data.custom_fields` | body | `object` | no | Campos personalizados da empresa. |
| `data.description` | body | `string` | no | Descrição da empresa. |
| `data.follower_ids[]` | body | `array<string>` | no | IDs dos usuários seguidores da empresa. |
| `data.name` | body | `string` | no | Nome da empresa. |
| `data.owner_id` | body | `string` | no | ID do usuário responsável pela empresa. |
| `data.segment_ids[]` | body | `array<string>` | no | IDs dos segmentos da empresa. |
| `data.url` | body | `string` | no | Site da empresa. |
| `id` | path | `string` | yes | Organization identifier. |
