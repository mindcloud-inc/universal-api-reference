# Documint: Update Template

Updates an existing template in Documint.

```
PUT https://connect.mindcloud.co/v1/universal/documint/latest/actions/update-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/documint/latest/actions/update-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "69bac297724eda8b0297192e",
  "name": "Updated Template"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/documint/latest/actions/update-template', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "69bac297724eda8b0297192e",
    "name": "Updated Template"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The Documint template ID to update. Example: `69bac297724eda8b0297192e`. |
| `name` | string | yes | Updated name for the template. Example: `Updated Template`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "id": "string",
      "name": "Ava Chen",
      "options": {},
      "tags": [
        "string"
      ],
      "testData": {},
      "thumbnail": {},
      "type": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `id` | string |  |
| `name` | string |  |
| `options` | object |  |
| `tags` | array<string> |  |
| `testData` | object |  |
| `thumbnail` | object |  |
| `type` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Documint API, this operation is `PUT /templates/:id` (base URL `https://api.documint.me/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-template.md) for the provider-specific parameters and requirements.

