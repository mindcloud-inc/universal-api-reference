# Update Contact with RD Station CRM

Updates an existing contact in RD Station CRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/:id`
- **Base URL:** `https://api.rd.services/crm/v2`
- **Official documentation:** [Update Contact](https://developers.rdstation.com/reference/crm-v2-update-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | yes | Contact payload documented in endpoint reference. |
| `data.birthday` | body | `date` | no | Data de aniversário do contato. Formato: YYYY-MM-DD. |
| `data.custom_fields` | body | `object` | no | Campos personalizados do contato. |
| `data.emails[]` | body | `array<object>` | no | Emails do contato. |
| `data.emails[].email` | body | `string` | no | Endereço de email. |
| `data.job_title` | body | `string` | no | Cargo do contato. |
| `data.legal_bases[]` | body | `array<object>` | no | Bases legais para o contato. |
| `data.legal_bases[].category` | body | `list` | no | Categoria da base legal. Accepted values: `0`. |
| `data.legal_bases[].status` | body | `list` | no | Status da base legal. Accepted values: `0`, `1`. |
| `data.legal_bases[].type` | body | `list` | no | Tipo da base legal. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`. |
| `data.name` | body | `string` | no | Nome do contato. |
| `data.organization_id` | body | `string` | no | ID da organização. |
| `data.phones[]` | body | `array<object>` | no | Telefones do contato. |
| `data.phones[].phone` | body | `string` | no | Telefone. |
| `data.phones[].type` | body | `list` | no | Tipo do telefone. Accepted values: `0`, `1`, `2`, `3`. |
| `data.social_profiles[]` | body | `array<object>` | no | Perfis sociais do contato. |
| `data.social_profiles[].type` | body | `list` | no | Tipo de perfil social. Accepted values: `0`, `1`, `2`. |
| `data.social_profiles[].username` | body | `string` | no | Nome de usuário. |
| `id` | path | `string` | yes | Contact identifier. |
