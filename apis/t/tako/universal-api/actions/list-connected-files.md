# Tako: List Connected Files

Retrieves connected files from Tako.

```
GET https://connect.mindcloud.co/v1/universal/tako/latest/actions/list-connected-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tako `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tako/latest/actions/list-connected-files?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tako/latest/actions/list-connected-files?${params}`, {
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
| `fileId` | string | no | Optional file ID to fetch one connected file instead of the full list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "files": [
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
| `files` | array<object> | List of files that were connected to |

## Native endpoint

Through the native Tako API, this operation is `GET /v1/beta/file_connector` (base URL `https://tako.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-connected-files.md) for the provider-specific parameters and requirements.

