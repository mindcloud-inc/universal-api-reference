# Ayrshare: Recommend Hashtags

Finds hashtag suggestions by keyword in Ayrshare.

```
GET https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/recommend-hashtags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ayrshare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/recommend-hashtags?connectionId=$CONNECTION_ID&keyword=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "keyword": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/recommend-hashtags?${params}`, {
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
| `keyword` | string | yes | Single keyword to get recommended hashtags from TikTok. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "hashtags": [
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
| `hashtags` | array<object> | Recommended hashtag records. |
| `message` | string | Recommendation or error message. |
| `status` | string | Response status. |

## Native endpoint

Through the native Ayrshare API, this operation is `GET /hashtags/recommend` (base URL `https://api.ayrshare.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/recommend-hashtags.md) for the provider-specific parameters and requirements.

