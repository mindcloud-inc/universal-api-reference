# Twitch: Delete Custom Reward

Deletes a custom reward from Twitch.

```
DELETE https://connect.mindcloud.co/v1/universal/twitch/latest/actions/delete-custom-reward
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twitch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/twitch/latest/actions/delete-custom-reward?connectionId=$CONNECTION_ID&broadcasterId=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "broadcasterId": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twitch/latest/actions/delete-custom-reward?${params}`, {
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
| `broadcasterId` | string | yes | The ID of the broadcaster that created the custom reward. |
| `id` | string | yes | The ID of the custom reward to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string | Empty response body returned when the custom reward is deleted successfully. |

## Native endpoint

Through the native Twitch API, this operation is `DELETE /channel_points/custom_rewards` (base URL `https://api.twitch.tv/helix`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-custom-reward.md) for the provider-specific parameters and requirements.

