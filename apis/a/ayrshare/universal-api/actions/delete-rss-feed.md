# Ayrshare: Delete RSS Feed

Deletes an RSS feed from Ayrshare.

```
DELETE https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/delete-rss-feed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ayrshare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/delete-rss-feed?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/delete-rss-feed?${params}`, {
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
| `id` | string | yes | Ayrshare RSS feed ID to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "id": "string",
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
| `id` | string | Deleted feed ID. |
| `message` | string | Delete feed or error message. |
| `status` | string | Delete feed status. |

## Native endpoint

Through the native Ayrshare API, this operation is `DELETE /feed` (base URL `https://api.ayrshare.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-rss-feed.md) for the provider-specific parameters and requirements.

