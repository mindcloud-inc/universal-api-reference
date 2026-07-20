# Socket: Search Dependencies

Finds dependencies used in Socket by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/socket/latest/actions/search-dependencies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socket/latest/actions/search-dependencies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socket/latest/actions/search-dependencies?${params}`, {
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
| `purls` | list<string> | no | PURLs to filter results with |

## Response

```json
{
  "success": true,
  "data": [
    {
      "end": true,
      "limit": 1,
      "offset": 1,
      "purlFilters": {
        "invalid": [
          "https://example.com"
        ],
        "valid": [
          "https://example.com"
        ]
      },
      "rows": [
        {
          "branch": "string",
          "direct": true,
          "id": "string",
          "name": "Ava Chen",
          "namespace": "Ava Chen",
          "release": "string",
          "repository": "string",
          "type": "string",
          "version": "string",
          "workspace": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `end` | boolean |  |
| `limit` | number |  |
| `offset` | number |  |
| `purlFilters` | object |  |
| `purlFilters.invalid` | array<string> |  |
| `purlFilters.valid` | array<string> |  |
| `rows` | array<object> |  |
| `rows[]` | object |  |
| `rows[].branch` | string |  |
| `rows[].direct` | boolean |  |
| `rows[].id` | string |  |
| `rows[].name` | string |  |
| `rows[].namespace` | string |  |
| `rows[].release` | string |  |
| `rows[].repository` | string |  |
| `rows[].type` | string |  |
| `rows[].version` | string |  |
| `rows[].workspace` | string |  |

## Native endpoint

Through the native Socket API, this operation is `POST /dependencies/search` (base URL `https://api.socket.dev/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-dependencies.md) for the provider-specific parameters and requirements.

