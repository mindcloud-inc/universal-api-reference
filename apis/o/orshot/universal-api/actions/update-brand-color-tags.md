# Orshot: Update Brand Color Tags



```
PUT https://connect.mindcloud.co/v1/universal/orshot/latest/actions/update-brand-color-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orshot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/orshot/latest/actions/update-brand-color-tags" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "tags[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/orshot/latest/actions/update-brand-color-tags', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "tags[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The saved brand color ID. |
| `tags[]` | array<string> | yes | The tags to set on the color, replacing existing tags. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "tags": [
        "string"
      ],
      "type": "string",
      "userId": "string",
      "value": "string",
      "workspaceId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `id` | number |  |
| `tags` | array<string> |  |
| `type` | string |  |
| `userId` | string |  |
| `value` | string |  |
| `workspaceId` | number |  |

## Native endpoint

Through the native Orshot API, this operation is `PATCH /brand-assets/colors/update/:id` (base URL `https://api.orshot.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-brand-color-tags.md) for the provider-specific parameters and requirements.

