# Spoki: Create Template

Creates a WhatsApp template for the authenticated account or a specific active WhatsApp channel.

```
POST https://connect.mindcloud.co/v1/universal/spoki/latest/actions/create-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoki `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/spoki/latest/actions/create-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "payload": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/spoki/latest/actions/create-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "payload": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `payload` | object | yes | Template fields to create, using Spoki's template schema. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "customfieldSet": [
        "string"
      ],
      "id": 1,
      "integration": 1,
      "isApproved": true,
      "isFavorite": true,
      "name": "Ava Chen",
      "subcategory": "string",
      "templateGroups": [
        {}
      ],
      "templatelocalizationSet": [
        {}
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
| `customfieldSet` | array<string> |  |
| `id` | number |  |
| `integration` | number |  |
| `isApproved` | boolean |  |
| `isFavorite` | boolean |  |
| `name` | string |  |
| `subcategory` | string |  |
| `templateGroups` | array<object> |  |
| `templatelocalizationSet` | array<object> |  |

## Native endpoint

Through the native Spoki API, this operation is `POST /templates/` (base URL `https://api.spoki.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-template.md) for the provider-specific parameters and requirements.

