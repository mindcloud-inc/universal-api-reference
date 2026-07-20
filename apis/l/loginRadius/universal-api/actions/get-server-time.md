# LoginRadius: Get Server Time

Retrieves current server time from LoginRadius.

```
GET https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/get-server-time
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LoginRadius `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/get-server-time?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/get-server-time?${params}`, {
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
      "currentTime": "string",
      "serverLocation": "string",
      "serverName": "Ava Chen",
      "sott": {
        "endTime": "string",
        "forWardedIP": "string",
        "ip": "string",
        "startTime": "string",
        "timeDifference": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentTime` | string |  |
| `serverLocation` | string |  |
| `serverName` | string |  |
| `sott.endTime` | string |  |
| `sott.forWardedIP` | string |  |
| `sott.ip` | string |  |
| `sott.startTime` | string |  |
| `sott.timeDifference` | string |  |

## Native endpoint

Through the native LoginRadius API, this operation is `GET /identity/v2/serverinfo` (base URL `https://api.loginradius.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-server-time.md) for the provider-specific parameters and requirements.

