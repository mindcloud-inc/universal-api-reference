# Update Deal with RD Station CRM

Updates an existing deal in RD Station CRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/deals/:id`
- **Base URL:** `https://api.rd.services/crm/v2`
- **Official documentation:** [Update Deal](https://developers.rdstation.com/reference/crm-v2-update-deal)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | yes | Deal payload documented in endpoint reference. |
| `data.campaign_id` | body | `string` | no | ID da campanha da negociação. |
| `data.contact_ids[]` | body | `array<string>` | no | IDs dos contatos associados à negociação. |
| `data.custom_fields` | body | `object` | no | Campos personalizados da negociação. |
| `data.distribution_settings` | body | `object` | no | Configurações de distribuição da negociação. |
| `data.expected_close_date` | body | `date` | no | Data de previsão de fechamento da negociação. |
| `data.lost_reason_id` | body | `string` | no | ID do motivo de perda da negociação. |
| `data.name` | body | `string` | no | Nome da negociação. |
| `data.one_time_price` | body | `number` | no | Valor único da negociação. |
| `data.organization_id` | body | `string` | no | ID da empresa associada à negociação. |
| `data.owner_id` | body | `string` | no | ID do usuário responsável pela negociação. |
| `data.rating` | body | `number` | no | Qualificação da negociação. |
| `data.recurrence_price` | body | `number` | no | Valor recorrente da negociação. |
| `data.source_id` | body | `string` | no | ID da fonte da negociação. |
| `data.stage_id` | body | `string` | no | ID da etapa do funil de vendas da negociação. |
| `data.status` | body | `string` | no | Status da negociação. |
| `id` | path | `string` | yes | Deal identifier. |
