# Ayrshare: Search Hashtags

Searches hashtag posts in Ayrshare.

```
GET https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/search-hashtags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ayrshare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/search-hashtags?connectionId=$CONNECTION_ID&keyword=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "keyword": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/search-hashtags?${params}`, {
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
| `keyword` | string | yes | Hashtag keyword to search for public Instagram media. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `searchType` | string | no | Search type such as top or recent, when supported by Ayrshare. One of: `recent`, `top`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": [
        {}
      ],
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | Ayrshare error code. |
| `data` | array<object> | Hashtag search result records. |
| `message` | string | Search or error message. |
| `status` | string | Response status. |

## Native endpoint

Through the native Ayrshare API, this operation is `GET /hashtags/search` (base URL `https://api.ayrshare.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-hashtags.md) for the provider-specific parameters and requirements.

