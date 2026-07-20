# Routee: Create a Pool

Creates a new pool in Routee.

```
POST https://connect.mindcloud.co/v1/universal/routee/latest/actions/create-a-pool
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/routee/latest/actions/create-a-pool" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "poolName": "Ava Chen",
  "smsSettings": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/routee/latest/actions/create-a-pool', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "poolName": "Ava Chen",
    "smsSettings": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `poolName` | string | yes | The name of the pool. |
| `smsSettings` | object | yes | The SMS settings of the pool |

## Response

```json
{
  "success": true,
  "data": [
    {
      "poolId": "string",
      "poolName": "Ava Chen",
      "smsSettings": {
        "alphanumericSenderId": "string",
        "callback": {
          "strategy": "string",
          "url": "https://example.com"
        },
        "defaultCountry": "string",
        "geomatch": true,
        "inboundSMSCallbackUrl": "https://example.com",
        "multipleSender": [
          [
            {}
          ]
        ],
        "sticky": true,
        "transcode": true
      },
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `poolId` | string |  |
| `poolName` | string |  |
| `smsSettings` | object |  |
| `smsSettings.alphanumericSenderId` | string |  |
| `smsSettings.callback` | object |  |
| `smsSettings.callback.strategy` | string |  |
| `smsSettings.callback.url` | string |  |
| `smsSettings.defaultCountry` | string |  |
| `smsSettings.geomatch` | boolean |  |
| `smsSettings.inboundSMSCallbackUrl` | string |  |
| `smsSettings.multipleSender[]` | array<object> |  |
| `smsSettings.multipleSender[].country` | string |  |
| `smsSettings.multipleSender[].keyword` | string |  |
| `smsSettings.multipleSender[].senderId` | string |  |
| `smsSettings.multipleSender[].shortCode` | string |  |
| `smsSettings.sticky` | boolean |  |
| `smsSettings.transcode` | boolean |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Routee API, this operation is `POST /pools/my` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-pool.md) for the provider-specific parameters and requirements.

