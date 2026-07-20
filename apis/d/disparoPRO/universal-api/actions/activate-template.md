# Disparo PRO: Activate Template

Updates a template to active in Disparo PRO.

```
PUT https://connect.mindcloud.co/v1/universal/disparoPRO/latest/actions/activate-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Disparo PRO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/disparoPRO/latest/actions/activate-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/disparoPRO/latest/actions/activate-template', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Template ID to activate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "contentType": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "language": "string",
      "name": "Ava Chen",
      "rejectionReason": "string",
      "reviewStatus": "string",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "variables": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `contentType` | object |  |
| `createdAt` | date |  |
| `id` | string |  |
| `language` | string |  |
| `name` | string |  |
| `rejectionReason` | string |  |
| `reviewStatus` | string |  |
| `status` | string |  |
| `updatedAt` | date |  |
| `variables` | array<string> |  |

## Native endpoint

Through the native Disparo PRO API, this operation is `PATCH /template/activate/:id` (base URL `https://gateway.disparopro.com.br/rcs`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/activate-template.md) for the provider-specific parameters and requirements.

