# Callbell: Create Custom Status

Creates a new custom status in Callbell.

```
POST https://connect.mindcloud.co/v1/universal/callbell/latest/actions/create-custom-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Callbell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/callbell/latest/actions/create-custom-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/callbell/latest/actions/create-custom-status', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name of the custom status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "emoji": "string",
      "id": "string",
      "name": "Ava Chen",
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
| `emoji` | string |  |
| `id` | string |  |
| `name` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Callbell API, this operation is `POST /custom_statuses` (base URL `https://api.callbell.eu/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-custom-status.md) for the provider-specific parameters and requirements.

