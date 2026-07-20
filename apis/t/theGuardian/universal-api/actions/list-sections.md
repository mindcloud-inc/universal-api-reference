# The Guardian: List Sections

Finds matching sections in The Guardian.

```
GET https://connect.mindcloud.co/v1/universal/theGuardian/latest/actions/list-sections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a The Guardian `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/theGuardian/latest/actions/list-sections?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/theGuardian/latest/actions/list-sections?${params}`, {
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
| `q` | string | no | Return sections matching this query term. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiUrl": "https://example.com",
      "editions": {
        "apiUrl": "https://example.com",
        "code": "string",
        "id": "string",
        "webTitle": "string",
        "webUrl": "https://example.com"
      },
      "id": "string",
      "webTitle": "string",
      "webUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiUrl` | string |  |
| `editions` | array<object> |  |
| `editions.apiUrl` | string |  |
| `editions.code` | string |  |
| `editions.id` | string |  |
| `editions.webTitle` | string |  |
| `editions.webUrl` | string |  |
| `id` | string |  |
| `webTitle` | string |  |
| `webUrl` | string |  |

## Native endpoint

Through the native The Guardian API, this operation is `GET /sections` (base URL `https://content.guardianapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sections.md) for the provider-specific parameters and requirements.

