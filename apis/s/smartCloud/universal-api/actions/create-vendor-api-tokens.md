# 2Smart Cloud: Create api token



```
POST https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/create-vendor-api-tokens
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Smart Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/create-vendor-api-tokens" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/create-vendor-api-tokens', {
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
| `name` | string | yes | Api Token name |

## Response

```json
{
  "success": true,
  "data": [
    {
      "access_token": "string",
      "created": "string",
      "id": 1,
      "name": "Ava Chen",
      "secret_token": "string",
      "updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access_token` | string |  |
| `created` | string |  |
| `id` | number |  |
| `name` | string |  |
| `secret_token` | string |  |
| `updated` | string |  |

## Native endpoint

Through the native 2Smart Cloud API, this operation is `POST /vendor/api-tokens` (base URL `https://cloud.2smart.com/robot/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-vendor-api-tokens.md) for the provider-specific parameters and requirements.

