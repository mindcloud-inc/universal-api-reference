# Unkey: Reroll Key

Rerolls an existing API key in Unkey.

```
PUT https://connect.mindcloud.co/v1/universal/unkey/latest/actions/reroll-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unkey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/unkey/latest/actions/reroll-key" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "keyId": "string",
  "expiration": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/unkey/latest/actions/reroll-key', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "keyId": "string",
    "expiration": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `keyId` | string | yes |  |
| `expiration` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "key": "string",
        "keyId": "string"
      },
      "meta": {
        "requestId": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.key` | string |  |
| `data.keyId` | string |  |
| `meta` | object |  |
| `meta.requestId` | string |  |

## Native endpoint

Through the native Unkey API, this operation is `POST /v2/keys.rerollKey` (base URL `https://api.unkey.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reroll-key.md) for the provider-specific parameters and requirements.

