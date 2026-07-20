# Landrr: Verify API Key

Retrieves API key verification details from Landrr.

```
GET https://connect.mindcloud.co/v1/universal/landrr/latest/actions/verify-api-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Landrr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/landrr/latest/actions/verify-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/landrr/latest/actions/verify-api-key?${params}`, {
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
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Landrr account email. |
| `id` | string | Landrr user ID. |
| `name` | string | Landrr account name. |
| `status` | number | HTTP status returned by the auth check. |

## Native endpoint

Through the native Landrr API, this operation is `GET /api/auth` (base URL `https://api.landrrapp.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-api-key.md) for the provider-specific parameters and requirements.

