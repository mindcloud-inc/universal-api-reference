# Kazm: List Files In Set

Retrieves files from a Kazm file set.

```
GET https://connect.mindcloud.co/v1/universal/kazm/latest/actions/list-files-in-set
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kazm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kazm/latest/actions/list-files-in-set?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kazm/latest/actions/list-files-in-set?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "files": [
        {}
      ],
      "has_more": true,
      "next_cursor": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `files` | array<object> |  |
| `has_more` | boolean |  |
| `next_cursor` | string |  |
| `total` | number |  |

## Native endpoint

Through the native Kazm API, this operation is `GET /filesets/:fileSetId/files` (base URL `https://api.lightningrod.ai/api/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-files-in-set.md) for the provider-specific parameters and requirements.

