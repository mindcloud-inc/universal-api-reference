# Gorgias: Search Resources

Finds resources in Gorgias by query.

```
GET https://connect.mindcloud.co/v1/universal/gorgias/latest/actions/search-resources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gorgias `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gorgias/latest/actions/search-resources?connectionId=$CONNECTION_ID&limit=25&offset=0&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gorgias/latest/actions/search-resources?${params}`, {
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
| `query` | string | yes | Search query text. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "meta": {},
      "object": "string",
      "uri": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `meta` | object |  |
| `object` | string |  |
| `uri` | string |  |

## Native endpoint

Through the native Gorgias API, this operation is `GET /search` (base URL `https://{{credentials.subdomain}}.gorgias.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-resources.md) for the provider-specific parameters and requirements.

