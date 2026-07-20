# JmpTo: List QR Codes

Retrieves QR codes from JmpTo.

```
GET https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/list-qr-codes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JmpTo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/list-qr-codes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/list-qr-codes?${params}`, {
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
      "date": "string",
      "id": 1,
      "link": "https://example.com",
      "name": "Ava Chen",
      "scans": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | string |  |
| `id` | number |  |
| `link` | string |  |
| `name` | string |  |
| `scans` | number |  |

## Native endpoint

Through the native JmpTo API, this operation is `GET /qr` (base URL `https://jmpto.net/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-qr-codes.md) for the provider-specific parameters and requirements.

