# SeaX: Update Phone

Updates a phone number in the current SeaX workspace.

```
PUT https://connect.mindcloud.co/v1/universal/seaX/latest/actions/update-phone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeaX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/seaX/latest/actions/update-phone" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "phoneId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seaX/latest/actions/update-phone', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "phoneId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `phoneId` | string | yes | Phone identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country": "string",
      "created_time": "string",
      "enabled": true,
      "enabled_dnc_reply": true,
      "enabled_generic_reply": true,
      "id": "string",
      "name": "Ava Chen",
      "phone": "string",
      "source": {},
      "type": {},
      "updated_time": "string",
      "users": [
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
| `country` | string |  |
| `created_time` | string |  |
| `enabled` | boolean |  |
| `enabled_dnc_reply` | boolean |  |
| `enabled_generic_reply` | boolean |  |
| `id` | string |  |
| `name` | string |  |
| `phone` | string |  |
| `source` | object |  |
| `type` | object |  |
| `updated_time` | string |  |
| `users` | array<object> |  |

## Native endpoint

Through the native SeaX API, this operation is `PATCH /phones/{phone_id}` (base URL `https://seax.seasalt.ai/seax-api/api/v1/workspace/{{credentials.workspaceId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-phone.md) for the provider-specific parameters and requirements.

