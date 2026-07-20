# Handelsregister AI: Search Organizations

Finds organizations in Handelsregister AI by search query.

```
GET https://connect.mindcloud.co/v1/universal/handelsregisterAI/latest/actions/search-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Handelsregister AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/handelsregisterAI/latest/actions/search-organizations?connectionId=$CONNECTION_ID&q=BMW%20AG" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "BMW AG"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/handelsregisterAI/latest/actions/search-organizations?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `q` | string | yes | Company name, registration number, or search query. Example: `BMW AG`. |
| `limit` | number | no | Maximum number of results to return (default: 10, max: 100). Default: `10`. Example: `10`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `skip` | number | no | Number of results to skip (default: 0). Default: `0`. Example: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "meta": {},
      "results": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `meta` | object | Request metadata. |
| `results` | array<object> | Matching organizations. |
| `total` | number | Total number of matches. |

## Native endpoint

Through the native Handelsregister AI API, this operation is `GET /search-organizations` (base URL `https://handelsregister.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-organizations.md) for the provider-specific parameters and requirements.

