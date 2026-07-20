# Vooplayer: Delete Videos

Deletes one or more videos from Vooplayer.

```
DELETE https://connect.mindcloud.co/v1/universal/vooplayer/latest/actions/delete-videos
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vooplayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/vooplayer/latest/actions/delete-videos?connectionId=$CONNECTION_ID&ids%5B%5D=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ids[]": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vooplayer/latest/actions/delete-videos?${params}`, {
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
| `ids[]` | array<number> | yes | Array of video IDs to delete. Accepts multiple values as an array. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Vooplayer API returns.

## Native endpoint

Through the native Vooplayer API, this operation is `POST /api/deleteVideo` (base URL `https://api.spotlightr.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-videos.md) for the provider-specific parameters and requirements.

