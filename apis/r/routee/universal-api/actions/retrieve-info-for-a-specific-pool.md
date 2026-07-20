# Routee: Retrieve info for a specific Pool

Retrieves info for a specific pool from Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-info-for-a-specific-pool
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-info-for-a-specific-pool?connectionId=$CONNECTION_ID&poolid=string&poolId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "poolid": "string",
  "poolId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-info-for-a-specific-pool?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `poolid` | string | yes | The tracking id of the pool. |
| `poolId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "poolId": "string",
      "poolName": "Ava Chen",
      "smsSettings": {
        "callback": {
          "strategy": "string",
          "url": "https://example.com"
        },
        "defaultCountry": "string",
        "geomatch": true,
        "sticky": true,
        "transcode": true
      },
      "totalNumbers": 1,
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
| `smsSettings.callback` | object |  |
| `smsSettings.callback.strategy` | string |  |
| `smsSettings.callback.url` | string |  |
| `smsSettings.defaultCountry` | string |  |
| `smsSettings.geomatch` | boolean |  |
| `smsSettings.sticky` | boolean |  |
| `smsSettings.transcode` | boolean |  |
| `totalNumbers` | number |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Routee API, this operation is `GET /pools/my/:poolId` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-info-for-a-specific-pool.md) for the provider-specific parameters and requirements.

