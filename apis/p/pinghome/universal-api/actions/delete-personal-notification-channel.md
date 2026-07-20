# Pinghome: Delete Personal Notification Channel

Deletes an existing personal notification channel from Pinghome.

```
DELETE https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/delete-personal-notification-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinghome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/delete-personal-notification-channel?connectionId=$CONNECTION_ID&id=string&priority=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "priority": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/delete-personal-notification-channel?${params}`, {
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
| `id` | string | yes | The unique ID of the customer. |
| `priority` | number | yes | The priority number of the notification channel to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pinghome API returns.

## Native endpoint

Through the native Pinghome API, this operation is `DELETE /customer-cmd/v1/customer/:id/notification-channel` (base URL `https://api.pinghome.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-personal-notification-channel.md) for the provider-specific parameters and requirements.

