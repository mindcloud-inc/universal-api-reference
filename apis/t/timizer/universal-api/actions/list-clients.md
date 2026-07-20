# Timizer: List Clients

Retrieves clients from Timizer.

```
GET https://connect.mindcloud.co/v1/universal/timizer/latest/actions/list-clients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timizer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timizer/latest/actions/list-clients?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timizer/latest/actions/list-clients?${params}`, {
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
      "companies": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companies` | array<object> |  |

## Native endpoint

Through the native Timizer API, this operation is `GET /app/clients` (base URL `https://api.timizer.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-clients.md) for the provider-specific parameters and requirements.

