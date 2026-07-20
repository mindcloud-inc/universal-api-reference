# Routee: Edit a Pool

Updates an existing pool in Routee.

```
PUT https://connect.mindcloud.co/v1/universal/routee/latest/actions/edit-a-pool
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/routee/latest/actions/edit-a-pool" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "poolId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/routee/latest/actions/edit-a-pool', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "poolId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `poolId` | string | yes | The tracking id of the pool. |
| `poolName` | string | no | The name of the pool. |
| `smsSettings` | object | no | The SMS settings of the pool. |

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
        "geomatch": true,
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
| `smsSettings.geomatch` | boolean |  |
| `smsSettings.sticky` | boolean |  |
| `smsSettings.transcode` | boolean |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Routee API, this operation is `PUT /pools/my/:poolId` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/edit-a-pool.md) for the provider-specific parameters and requirements.

