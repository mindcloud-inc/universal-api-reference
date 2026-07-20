# Ayrshare: List Platform Post History

Retrieves post history for a platform from Ayrshare.

```
GET https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/list-platform-post-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ayrshare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/list-platform-post-history?connectionId=$CONNECTION_ID&platform=bluesky" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "platform": "bluesky"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/list-platform-post-history?${params}`, {
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
| `platform` | string | yes | Social network platform, such as instagram, facebook, twitter, linkedin, or youtube. One of: `bluesky`, `facebook`, `gmb`, `instagram`, `linkedin`, `pinterest`, `reddit`, `snapchat`, `telegram`, `threads`, `tiktok`, `twitter`, `youtube`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "history": [
        {}
      ],
      "message": "string",
      "next": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `history` | array<object> | Platform post history records. |
| `message` | string | Status or error message. |
| `next` | string | Pagination token for the next page when returned. |
| `status` | string | Response status. |

## Native endpoint

Through the native Ayrshare API, this operation is `GET /history/:platform` (base URL `https://api.ayrshare.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-platform-post-history.md) for the provider-specific parameters and requirements.

