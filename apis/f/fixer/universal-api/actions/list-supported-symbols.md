# Fixer: List Supported Symbols

Retrieves supported currency symbols from Fixer.

```
GET https://connect.mindcloud.co/v1/universal/fixer/latest/actions/list-supported-symbols
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fixer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fixer/latest/actions/list-supported-symbols?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fixer/latest/actions/list-supported-symbols?${params}`, {
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
      "code": "string",
      "description": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Three-letter ISO currency code. |
| `description` | string | Human-readable currency name. |

## Native endpoint

Through the native Fixer API, this operation is `GET /symbols` (base URL `https://data.fixer.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-supported-symbols.md) for the provider-specific parameters and requirements.

