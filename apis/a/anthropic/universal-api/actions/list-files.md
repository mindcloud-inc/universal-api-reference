# Anthropic: List Files

Retrieves uploaded files from the Anthropic account.

```
GET https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/list-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anthropic `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/list-files?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/list-files?${params}`, {
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
| `limit` | number | no | Maximum number of files to return. Example: `20`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `afterId` | string | no | Return items after this file ID for forward pagination. Example: `file_abc123`. |
| `beforeId` | string | no | Return items before this file ID for reverse pagination. Example: `file_abc123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "firstId": "string",
      "hasMore": true,
      "lastId": "string",
      "nextPage": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | List of files. |
| `firstId` | string | First file ID in page. |
| `hasMore` | boolean | Whether more pages are available. |
| `lastId` | string | Last file ID in page. |
| `nextPage` | string | Opaque token for the next page. |

## Native endpoint

Through the native Anthropic API, this operation is `GET /v1/files` (base URL `https://api.anthropic.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-files.md) for the provider-specific parameters and requirements.

