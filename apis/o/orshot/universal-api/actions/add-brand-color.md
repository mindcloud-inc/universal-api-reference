# Orshot: Add Brand Color



```
POST https://connect.mindcloud.co/v1/universal/orshot/latest/actions/add-brand-color
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orshot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/orshot/latest/actions/add-brand-color" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/orshot/latest/actions/add-brand-color', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "value": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | The display name for the color. |
| `tags[]` | array<string> | no | Tags to associate with the color. |
| `value` | string | yes | The hex value for the color. |

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

Through the native Orshot API, this operation is `POST /brand-assets/colors/add` (base URL `https://api.orshot.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-brand-color.md) for the provider-specific parameters and requirements.

