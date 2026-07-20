# Liveblocks: Get Room Subscription Settings

Retrieves room subscription settings from Liveblocks.

```
GET https://connect.mindcloud.co/v1/universal/liveblocks/latest/actions/get-room-subscription-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Liveblocks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/liveblocks/latest/actions/get-room-subscription-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/liveblocks/latest/actions/get-room-subscription-settings?${params}`, {
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
| `userId` | string | no | ID of the user. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "settings": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `settings` | object | Room subscription settings. |

## Native endpoint

Through the native Liveblocks API, this operation is `GET /rooms/:roomId/users/:userId/subscription-settings` (base URL `https://api.liveblocks.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-room-subscription-settings.md) for the provider-specific parameters and requirements.

