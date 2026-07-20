# Restream: Delete Channel

Deletes a streaming channel from Restream.

```
DELETE https://connect.mindcloud.co/v1/universal/restream/latest/actions/delete-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Restream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/restream/latest/actions/delete-channel?connectionId=$CONNECTION_ID&channelId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channelId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/restream/latest/actions/delete-channel?${params}`, {
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
| `channelId` | number | yes | The ID of the channel to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Restream API returns.

## Native endpoint

Through the native Restream API, this operation is `DELETE /user/channels/:channelId` (base URL `https://api.restream.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-channel.md) for the provider-specific parameters and requirements.

