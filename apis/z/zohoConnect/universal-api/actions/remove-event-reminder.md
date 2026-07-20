# Zoho Connect: Remove Event Reminder

Removes a reminder from a Zoho Connect event.

```
DELETE https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/remove-event-reminder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Connect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/remove-event-reminder?connectionId=$CONNECTION_ID&scopeId=string&streamId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "scopeId": "string",
  "streamId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/remove-event-reminder?${params}`, {
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
| `scopeId` | string | yes |  |
| `streamId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleteEventReminder": {
        "result": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleteEventReminder.result` | string |  |

## Native endpoint

Through the native Zoho Connect API, this operation is `DELETE /pulse/api/deleteEventReminder` (base URL `https://connect.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-event-reminder.md) for the provider-specific parameters and requirements.

