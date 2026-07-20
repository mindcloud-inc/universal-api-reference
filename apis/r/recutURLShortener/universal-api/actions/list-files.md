# Recut URL Shortener: List Files

Retrieves files from Recut URL Shortener.

```
GET https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/list-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recut URL Shortener `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/list-files?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/list-files?${params}`, {
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
| `name` | string | no | Filter files by name Example: `invoice`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currentpage": 1,
      "error": 1,
      "list": [
        {}
      ],
      "maxpage": 1,
      "nextpage": 1,
      "perpage": 1,
      "result": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentpage` | number |  |
| `error` | number |  |
| `list` | array<object> |  |
| `maxpage` | number |  |
| `nextpage` | number |  |
| `perpage` | number |  |
| `result` | number |  |

## Native endpoint

Through the native Recut URL Shortener API, this operation is `GET /files` (base URL `https://app.recut.in/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-files.md) for the provider-specific parameters and requirements.

