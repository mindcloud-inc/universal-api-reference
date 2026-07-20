# Date & Time: Get Date & Time Service Overview



```
GET https://connect.mindcloud.co/v1/universal/dateTime/latest/actions/get-date-time-service-overview
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Date & Time `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dateTime/latest/actions/get-date-time-service-overview?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dateTime/latest/actions/get-date-time-service-overview?${params}`, {
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
      "channel": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channel` | object | Get Date & Time Service Overview response root. |

## Native endpoint

Through the native Date & Time API, this operation is `POST api/v3/graph` (base URL `https://ifttt.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-date-time-service-overview.md) for the provider-specific parameters and requirements.

