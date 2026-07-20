# Reflect: List Links

Retrieves links from a graph in Reflect.

```
GET https://connect.mindcloud.co/v1/universal/reflect/latest/actions/list-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reflect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reflect/latest/actions/list-links?connectionId=$CONNECTION_ID&graphId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "graphId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reflect/latest/actions/list-links?${params}`, {
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
| `graphId` | list<string> | yes | Your graph identifier |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "highlights": [
        "string"
      ],
      "id": "string",
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `highlights` | array<string> |  |
| `id` | string |  |
| `title` | string |  |
| `updatedAt` | date |  |
| `url` | string |  |

## Native endpoint

Through the native Reflect API, this operation is `GET /graphs/:graphId/links` (base URL `https://reflect.app/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-links.md) for the provider-specific parameters and requirements.

