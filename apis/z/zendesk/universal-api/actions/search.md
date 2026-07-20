# Zendesk: Search

Finds records in Zendesk by search query.

```
GET https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zendesk `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/search?connectionId=$CONNECTION_ID&limit=25&offset=0&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/search?${params}`, {
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
| `query` | string | yes | Search query string. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen",
      "resultType": "string",
      "subject": "string",
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
| `createdAt` | date | Creation timestamp when present on the matched resource. |
| `id` | number | Search result id. |
| `name` | string | Name field when present on the matched resource. |
| `resultType` | string | Type of the matched resource. |
| `subject` | string | Subject field when present on the matched resource. |
| `updatedAt` | date | Last update timestamp when present on the matched resource. |
| `url` | string | URL of the matched resource. |

## Native endpoint

Through the native Zendesk API, this operation is `GET /search.json` (base URL `https://{{credentials.subdomain}}.zendesk.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search.md) for the provider-specific parameters and requirements.

