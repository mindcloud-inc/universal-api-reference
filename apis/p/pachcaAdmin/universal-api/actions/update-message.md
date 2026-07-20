# Pachca (Admin): Update Message

Updates an existing message in the Pachca Admin API.

```
PUT https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/update-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pachca (Admin) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/update-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "message.content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/update-message', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "message.content": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The Pachca message ID. |
| `message.content` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |

## Native endpoint

Through the native Pachca (Admin) API, this operation is `PUT /messages/:id` (base URL `https://api.pachca.com/api/shared/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-message.md) for the provider-specific parameters and requirements.

