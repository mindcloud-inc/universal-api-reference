# GetResponse: Get Sending Limits

Retrieves current sending limits from GetResponse.

```
GET https://connect.mindcloud.co/v1/universal/getResponse/latest/actions/get-sending-limits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GetResponse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/getResponse/latest/actions/get-sending-limits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/getResponse/latest/actions/get-sending-limits?${params}`, {
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
      "limit": 1,
      "timeFrame": 1,
      "used": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `limit` | number |  |
| `timeFrame` | number |  |
| `used` | number |  |

## Native endpoint

Through the native GetResponse API, this operation is `GET /accounts/sending-limits` (base URL `https://api.getresponse.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sending-limits.md) for the provider-specific parameters and requirements.

