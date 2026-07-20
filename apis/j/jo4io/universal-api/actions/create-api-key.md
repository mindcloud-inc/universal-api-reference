# jo4.io: Create API Key



```
POST https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/create-api-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a jo4.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/create-api-key" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/create-api-key', {
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
| `description` | string | no |  |
| `expiresAt` | number | no |  |
| `name` | string | yes |  |
| `scopes` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiKey": "string",
      "createdTime": 1,
      "description": "string",
      "expiresAt": 1,
      "id": 1,
      "keyPrefix": "string",
      "name": "Ava Chen",
      "scopes": [
        "string"
      ],
      "slug": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiKey` | string |  |
| `createdTime` | number |  |
| `description` | string |  |
| `expiresAt` | number |  |
| `id` | number |  |
| `keyPrefix` | string |  |
| `name` | string |  |
| `scopes` | array<string> |  |
| `slug` | string |  |

## Native endpoint

Through the native jo4.io API, this operation is `POST /protected/api-keys` (base URL `https://jo4-api.jo4.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-api-key.md) for the provider-specific parameters and requirements.

