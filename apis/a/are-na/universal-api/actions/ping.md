# Are.na: Ping

Retrieves API health status from Are.na.

```
GET https://connect.mindcloud.co/v1/universal/are-na/latest/actions/ping
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Are.na `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/are-na/latest/actions/ping?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/are-na/latest/actions/ping?${params}`, {
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
      "message": "string",
      "status": "string",
      "timestamp": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `status` | string |  |
| `timestamp` | date |  |

## Native endpoint

Through the native Are.na API, this operation is `GET ping` (base URL `https://api.are.na/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/ping.md) for the provider-specific parameters and requirements.

