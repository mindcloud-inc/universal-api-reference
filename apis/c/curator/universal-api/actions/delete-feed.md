# Curator: Delete Feed

Deletes an existing feed from Curator.

```
DELETE https://connect.mindcloud.co/v1/universal/curator/latest/actions/delete-feed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Curator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/curator/latest/actions/delete-feed?connectionId=$CONNECTION_ID&feedId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "feedId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/curator/latest/actions/delete-feed?${params}`, {
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
| `feedId` | string | yes | ID of the feed to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Curator API, this operation is `DELETE /v1/feeds/:FEED_ID` (base URL `https://api.curator.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-feed.md) for the provider-specific parameters and requirements.

