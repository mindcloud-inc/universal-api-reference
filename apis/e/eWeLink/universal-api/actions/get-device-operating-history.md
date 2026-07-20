# eWeLink: Get Device Operating History

Retrieves device operating history from eWeLink.

```
GET https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/get-device-operating-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eWeLink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/get-device-operating-history?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/get-device-operating-history?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "histories": [
        {
          "deviceid": "string",
          "opsAccount": "string",
          "opsSwitchs": "string",
          "opsTime": 1,
          "request": "string",
          "userAgent": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `histories[].deviceid` | string |  |
| `histories[].opsAccount` | string |  |
| `histories[].opsSwitchs` | string |  |
| `histories[].opsTime` | number |  |
| `histories[].request` | string |  |
| `histories[].userAgent` | string |  |

## Native endpoint

Through the native eWeLink API, this operation is `GET /v2/device/history` (base URL `https://{{credentials.authorizeRequest.region}}-apia.coolkit.cc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-device-operating-history.md) for the provider-specific parameters and requirements.

