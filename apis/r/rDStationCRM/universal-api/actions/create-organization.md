# RD Station CRM: Create Organization

Creates a new organization in RD Station CRM.

```
POST https://connect.mindcloud.co/v1/universal/rDStationCRM/latest/actions/create-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RD Station CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rDStationCRM/latest/actions/create-organization" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rDStationCRM/latest/actions/create-organization', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | object | yes | Organization payload documented in endpoint reference. |
| `data.address` | object | no | Endereço da empresa. |
| `data.custom_fields` | object | no | Campos personalizados da empresa. |
| `data.description` | string | no | Descrição da empresa. |
| `data.follower_ids[]` | array<string> | no | IDs dos usuários seguidores da empresa. |
| `data.name` | string | no | Nome da empresa. |
| `data.owner_id` | string | no | ID do usuário responsável pela empresa. |
| `data.segment_ids[]` | array<string> | no | IDs dos segmentos da empresa. |
| `data.url` | string | no | Site da empresa. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "address": {},
        "createdAt": "string",
        "customFields": {},
        "followerIds": [
          [
            "string"
          ]
        ],
        "id": "string",
        "name": "Ava Chen",
        "ownerId": "string",
        "segmentIds": [
          [
            "string"
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
| `data.address` | object |  |
| `data.createdAt` | string |  |
| `data.customFields` | object |  |
| `data.followerIds[]` | array<string> |  |
| `data.id` | string |  |
| `data.name` | string |  |
| `data.ownerId` | string |  |
| `data.segmentIds[]` | array<string> |  |
| `data.updatedAt` | string |  |

## Native endpoint

Through the native RD Station CRM API, this operation is `POST /organizations` (base URL `https://api.rd.services/crm/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-organization.md) for the provider-specific parameters and requirements.

