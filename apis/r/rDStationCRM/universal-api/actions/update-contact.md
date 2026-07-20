# RD Station CRM: Update Contact

Updates an existing contact in RD Station CRM.

```
PUT https://connect.mindcloud.co/v1/universal/rDStationCRM/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RD Station CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rDStationCRM/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data": {},
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rDStationCRM/latest/actions/update-contact', {
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
| `data` | object | yes | Contact payload documented in endpoint reference. |
| `data.birthday` | date | no | Data de aniversário do contato. Formato: YYYY-MM-DD. |
| `data.custom_fields` | object | no | Campos personalizados do contato. |
| `data.emails[]` | array<object> | no | Emails do contato. |
| `data.emails[].email` | string | no | Endereço de email. |
| `data.job_title` | string | no | Cargo do contato. |
| `data.legal_bases[]` | array<object> | no | Bases legais para o contato. |
| `data.legal_bases[].category` | list | no | Categoria da base legal. One of: `0`. |
| `data.legal_bases[].status` | list | no | Status da base legal. One of: `0`, `1`. |
| `data.legal_bases[].type` | list | no | Tipo da base legal. One of: `0`, `1`, `2`, `3`, `4`, `5`. |
| `data.name` | string | no | Nome do contato. |
| `data.organization_id` | string | no | ID da organização. |
| `data.phones[]` | array<object> | no | Telefones do contato. |
| `data.phones[].phone` | string | no | Telefone. |
| `data.phones[].type` | list | no | Tipo do telefone. One of: `0`, `1`, `2`, `3`. |
| `data.social_profiles[]` | array<object> | no | Perfis sociais do contato. |
| `data.social_profiles[].type` | list | no | Tipo de perfil social. One of: `0`, `1`, `2`. |
| `data.social_profiles[].username` | string | no | Nome de usuário. |
| `id` | string | yes | Contact identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "contextOrigin": "string",
        "createdAt": "string",
        "customFields": {},
        "emails": [
          [
            {}
          ]
        ],
        "id": "string",
        "legalBases": [
          [
            {}
          ]
        ],
        "name": "Ava Chen",
        "phones": [
          [
            {}
          ]
        ],
        "socialProfiles": [
          [
            {}
          ]
        ],
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
| `data.contextOrigin` | string |  |
| `data.createdAt` | string |  |
| `data.customFields` | object |  |
| `data.emails[]` | array<object> |  |
| `data.emails[].email` | string |  |
| `data.id` | string |  |
| `data.legalBases[]` | array<object> |  |
| `data.legalBases[].category` | string |  |
| `data.legalBases[].status` | string |  |
| `data.legalBases[].type` | string |  |
| `data.name` | string |  |
| `data.phones[]` | array<object> |  |
| `data.phones[].phone` | string |  |
| `data.phones[].type` | string |  |
| `data.socialProfiles[]` | array<object> |  |
| `data.socialProfiles[].type` | string |  |
| `data.socialProfiles[].username` | string |  |
| `data.updatedAt` | string |  |

## Native endpoint

Through the native RD Station CRM API, this operation is `PUT /contacts/:id` (base URL `https://api.rd.services/crm/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

