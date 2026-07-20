# Superthread: List Pages



```
GET https://connect.mindcloud.co/v1/universal/superthread/latest/actions/list-pages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Superthread `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superthread/latest/actions/list-pages?connectionId=$CONNECTION_ID&teamId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superthread/latest/actions/list-pages?${params}`, {
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
| `archived` | boolean | no | Include archived pages when enabled. |
| `projectId` | string | no | Space ID used to scope pages. |
| `teamId` | string | yes | Workspace ID for the Superthread workspace. |
| `updatedRecently` | boolean | no | Limit results to recently updated pages when enabled. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archive_page_order": [
        "string"
      ],
      "count": 1,
      "cursor": "string",
      "page_order": [
        {}
      ],
      "pages": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archive_page_order` | array<string> |  |
| `count` | number |  |
| `cursor` | string |  |
| `page_order` | array<object> |  |
| `pages` | array<object> |  |

## Native endpoint

Through the native Superthread API, this operation is `GET /:team_id/pages` (base URL `https://api.superthread.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-pages.md) for the provider-specific parameters and requirements.

