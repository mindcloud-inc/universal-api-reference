# Liveblocks: Delete Room Subscription Settings

Deletes room subscription settings from Liveblocks.

```
DELETE https://connect.mindcloud.co/v1/universal/liveblocks/latest/actions/delete-room-subscription-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Liveblocks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/liveblocks/latest/actions/delete-room-subscription-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/liveblocks/latest/actions/delete-room-subscription-settings?${params}`, {
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
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the room subscription settings deletion request succeeded. |

## Native endpoint

Through the native Liveblocks API, this operation is `DELETE /rooms/:roomId/users/:userId/subscription-settings` (base URL `https://api.liveblocks.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-room-subscription-settings.md) for the provider-specific parameters and requirements.

