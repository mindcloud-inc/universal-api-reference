# Disparo PRO: Create Template

Creates a new template in Disparo PRO.

```
POST https://connect.mindcloud.co/v1/universal/disparoPRO/latest/actions/create-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Disparo PRO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/disparoPRO/latest/actions/create-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "language": "string",
  "category": "string",
  "name": "Ava Chen",
  "contentType": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/disparoPRO/latest/actions/create-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "language": "string",
    "category": "string",
    "name": "Ava Chen",
    "contentType": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `language` | string | yes | Language code for the template. |
| `category` | string | yes | Category of the RCS template. |
| `name` | string | yes | Unique template name. |
| `variables[]` | array<string> | no | Template variables for dynamic content substitution. |
| `contentType` | object | yes | Template content configuration. |
| `previousTemplateId` | string | no | Previous template version ID. |

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

Through the native Disparo PRO API, this operation is `POST /template` (base URL `https://gateway.disparopro.com.br/rcs`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-template.md) for the provider-specific parameters and requirements.

