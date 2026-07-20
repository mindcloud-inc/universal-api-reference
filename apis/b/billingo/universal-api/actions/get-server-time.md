# Billingo: Get Server Time

Retrieves the current server time from Billingo.

```
GET https://connect.mindcloud.co/v1/universal/billingo/latest/actions/get-server-time
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billingo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billingo/latest/actions/get-server-time?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billingo/latest/actions/get-server-time?${params}`, {
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
      "epoch": 1,
      "formatted": "string",
      "timezone": "string",
      "w3c": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `epoch` | number |  |
| `formatted` | string |  |
| `timezone` | string |  |
| `w3c` | string |  |

## Native endpoint

Through the native Billingo API, this operation is `GET /utils/time` (base URL `https://api.billingo.hu/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-server-time.md) for the provider-specific parameters and requirements.

