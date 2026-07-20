# Selock: List Locks



```
GET https://connect.mindcloud.co/v1/universal/selock/latest/actions/list-locks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Selock `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/selock/latest/actions/list-locks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/selock/latest/actions/list-locks?${params}`, {
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
      "data": {},
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Response envelope that contains the locks collection. |
| `result` | boolean | True when Selock accepted the request. |

## Native endpoint

Through the native Selock API, this operation is `POST /get_data/` (base URL `https://selock.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-locks.md) for the provider-specific parameters and requirements.

