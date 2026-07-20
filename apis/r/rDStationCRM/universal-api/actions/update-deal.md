# RD Station CRM: Update Deal

Updates an existing deal in RD Station CRM.

```
PUT https://connect.mindcloud.co/v1/universal/rDStationCRM/latest/actions/update-deal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RD Station CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rDStationCRM/latest/actions/update-deal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data": {},
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rDStationCRM/latest/actions/update-deal', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data": {},
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | object | yes | Deal payload documented in endpoint reference. |
| `data.campaign_id` | string | no | ID da campanha da negociação. |
| `data.contact_ids[]` | array<string> | no | IDs dos contatos associados à negociação. |
| `data.custom_fields` | object | no | Campos personalizados da negociação. |
| `data.distribution_settings` | object | no | Configurações de distribuição da negociação. |
| `data.expected_close_date` | date | no | Data de previsão de fechamento da negociação. |
| `data.lost_reason_id` | string | no | ID do motivo de perda da negociação. |
| `data.name` | string | no | Nome da negociação. |
| `data.one_time_price` | number | no | Valor único da negociação. |
| `data.organization_id` | string | no | ID da empresa associada à negociação. |
| `data.owner_id` | string | no | ID do usuário responsável pela negociação. |
| `data.rating` | number | no | Qualificação da negociação. |
| `data.recurrence_price` | number | no | Valor recorrente da negociação. |
| `data.source_id` | string | no | ID da fonte da negociação. |
| `data.stage_id` | string | no | ID da etapa do funil de vendas da negociação. |
| `data.status` | string | no | Status da negociação. |
| `id` | string | yes | Deal identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "contactIds": [
          [
            "string"
          ]
        ],
        "createdAt": "string",
        "customFields": {},
        "id": "string",
        "name": "Ava Chen",
        "oneTimePrice": 1,
        "ownerId": "string",
        "pipelineId": "string",
        "rating": 1,
        "recurrencePrice": 1,
        "stageId": "string",
        "status": "string",
        "totalPrice": 1,
        "updatedAt": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.contactIds[]` | array<string> |  |
| `data.createdAt` | string |  |
| `data.customFields` | object |  |
| `data.id` | string |  |
| `data.name` | string |  |
| `data.oneTimePrice` | number |  |
| `data.ownerId` | string |  |
| `data.pipelineId` | string |  |
| `data.rating` | number |  |
| `data.recurrencePrice` | number |  |
| `data.stageId` | string |  |
| `data.status` | string |  |
| `data.totalPrice` | number |  |
| `data.updatedAt` | string |  |

## Native endpoint

Through the native RD Station CRM API, this operation is `PUT /deals/:id` (base URL `https://api.rd.services/crm/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-deal.md) for the provider-specific parameters and requirements.

