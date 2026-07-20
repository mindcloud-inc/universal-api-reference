# Baserow: Check Database Token

Checks whether a Baserow API token is valid.

```
GET https://connect.mindcloud.co/v1/universal/baserow/latest/actions/check-database-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Baserow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/baserow/latest/actions/check-database-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/baserow/latest/actions/check-database-token?${params}`, {
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
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `token` | string |  |

## Native endpoint

Through the native Baserow API, this operation is `GET /api/database/tokens/check/` (base URL `https://api.baserow.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-database-token.md) for the provider-specific parameters and requirements.

