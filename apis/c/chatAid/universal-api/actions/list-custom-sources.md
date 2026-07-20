# Chat Aid: List Custom Sources

Retrieves custom sources from your Chat Aid workspace.

```
GET https://connect.mindcloud.co/v1/universal/chatAid/latest/actions/list-custom-sources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chat Aid `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatAid/latest/actions/list-custom-sources?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatAid/latest/actions/list-custom-sources?${params}`, {
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
| `name` | string | no | Filter sources by partial, case-insensitive name. Example: `Product Documentation`. |
| `status` | list | no | Filter sources by status. One of: `Active`, `Error`, `Processing`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | no | Filter sources by file type. Example: `pdf`. |
| `teamId` | string | no | Filter sources by team ID. Example: `team123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "status": "string",
      "type": "string",
      "url": "https://example.com",
      "usageCounts": 1,
      "wordCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `id` | string |  |
| `name` | string |  |
| `status` | string |  |
| `type` | string |  |
| `url` | string |  |
| `usageCounts` | number |  |
| `wordCount` | number |  |

## Native endpoint

Through the native Chat Aid API, this operation is `GET /external/sources/custom` (base URL `https://api.chataid.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-custom-sources.md) for the provider-specific parameters and requirements.

