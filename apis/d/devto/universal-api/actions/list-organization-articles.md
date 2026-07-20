# Dev.to: List Organization Articles

Lists articles for a Dev.to organization.

```
GET https://connect.mindcloud.co/v1/universal/devto/latest/actions/list-organization-articles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dev.to `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/devto/latest/actions/list-organization-articles?connectionId=$CONNECTION_ID&limit=25&offset=0&username=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "username": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/devto/latest/actions/list-organization-articles?${params}`, {
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
| `username` | string | yes | Organization username. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "id": 1,
      "path": "string",
      "published_timestamp": "2026-05-07T12:00:00.000Z",
      "tag_list": [
        "string"
      ],
      "title": "string",
      "url": "https://example.com",
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `id` | number |  |
| `path` | string |  |
| `published_timestamp` | date |  |
| `tag_list` | array<string> |  |
| `title` | string |  |
| `url` | string |  |
| `user` | object |  |

## Native endpoint

Through the native Dev.to API, this operation is `GET /organizations/:username/articles` (base URL `https://dev.to/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-organization-articles.md) for the provider-specific parameters and requirements.

