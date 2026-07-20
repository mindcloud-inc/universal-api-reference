# Spoki: Update Template

Updates an existing WhatsApp template by ID with partial changes.

```
PUT https://connect.mindcloud.co/v1/universal/spoki/latest/actions/update-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoki `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/spoki/latest/actions/update-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "payload": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/spoki/latest/actions/update-template', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "payload": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The template ID. |
| `payload` | object | yes | Template fields to update, using Spoki's template schema. |

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

Through the native Spoki API, this operation is `PATCH /templates/{{id}}/` (base URL `https://api.spoki.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-template.md) for the provider-specific parameters and requirements.

