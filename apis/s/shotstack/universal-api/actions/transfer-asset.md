# Shotstack: Transfer Asset



```
POST https://connect.mindcloud.co/v1/universal/shotstack/latest/actions/transfer-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shotstack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shotstack/latest/actions/transfer-asset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shotstack/latest/actions/transfer-asset', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | yes | The Shotstack request body. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "attributes": {
          "created": "string",
          "id": "string",
          "owner": "string",
          "status": "string"
        },
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.attributes.created` | string | Transfer creation timestamp. |
| `data.attributes.id` | string | Transferred asset identifier. |
| `data.attributes.owner` | string | Owner identifier for the transferred asset. |
| `data.attributes.status` | string | Current transfer status. |
| `data.type` | string | Resource type for the transfer. |

## Native endpoint

Through the native Shotstack API, this operation is `POST /serve/v1/assets` (base URL `https://api.shotstack.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/transfer-asset.md) for the provider-specific parameters and requirements.

