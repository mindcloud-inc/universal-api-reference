# Disparo PRO: Get Template

Retrieves a template from Disparo PRO.

```
GET https://connect.mindcloud.co/v1/universal/disparoPRO/latest/actions/get-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Disparo PRO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/disparoPRO/latest/actions/get-template?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/disparoPRO/latest/actions/get-template?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Template ID to find. |

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

Through the native Disparo PRO API, this operation is `GET /template/:id` (base URL `https://gateway.disparopro.com.br/rcs`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template.md) for the provider-specific parameters and requirements.

