# BASIC: Regenerate API key

Regenerates an API key in BASIC.

```
PUT https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/regenerate-api-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BASIC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/regenerate-api-key" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/regenerate-api-key', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "key": {
        "created_at": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "is_private": true,
        "label": "string",
        "roles": "string",
        "value": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `key.created_at` | date |  |
| `key.id` | string |  |
| `key.is_private` | boolean |  |
| `key.label` | string |  |
| `key.roles` | string |  |
| `key.value` | string |  |

## Native endpoint

Through the native BASIC API, this operation is `POST /project/{id}/key/{key_id}/regenerate` (base URL `https://api.basic.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/regenerate-api-key.md) for the provider-specific parameters and requirements.

