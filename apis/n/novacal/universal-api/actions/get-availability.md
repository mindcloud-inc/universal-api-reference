# Novacal: Get Availability

Retrieves availability from Novacal.

```
GET https://connect.mindcloud.co/v1/universal/novacal/latest/actions/get-availability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Novacal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/novacal/latest/actions/get-availability?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/novacal/latest/actions/get-availability?${params}`, {
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
      "availability": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availability` | object | Availability keyed by date, where each date contains available start/end ranges. |

## Native endpoint

Through the native Novacal API, this operation is `GET /v1/availability` (base URL `https://api.novacal.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-availability.md) for the provider-specific parameters and requirements.

