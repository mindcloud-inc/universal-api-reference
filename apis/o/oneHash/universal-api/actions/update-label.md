# OneHash: Update Label

Updates an existing label in OneHash.

```
PUT https://connect.mindcloud.co/v1/universal/oneHash/latest/actions/update-label
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneHash `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/oneHash/latest/actions/update-label" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oneHash/latest/actions/update-label', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string | no | OneHash Chat account id. |
| `color` | string | no | Hex color. |
| `description` | string | no | Label description. |
| `id` | string | no | Label id. |
| `title` | string | no | Label title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "description": "string",
      "id": 1,
      "showOnSidebar": true,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `description` | string |  |
| `id` | number |  |
| `showOnSidebar` | boolean |  |
| `title` | string |  |

## Native endpoint

Through the native OneHash API, this operation is `PATCH /api/v1/accounts/:accountId/labels/:id` (base URL `https://chat.onehash.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-label.md) for the provider-specific parameters and requirements.

