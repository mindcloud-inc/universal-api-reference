# smsmode: Cancel Scheduled RCS Message



```
DELETE https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/cancel-scheduled-rcs-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a smsmode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/cancel-scheduled-rcs-message?connectionId=$CONNECTION_ID&channelId=string&campaignId=string&messageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channelId": "string",
  "campaignId": "string",
  "messageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/cancel-scheduled-rcs-message?${params}`, {
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
| `channelId` | string | yes | Channel ID path parameter from the smsmode API route. |
| `campaignId` | string | yes | Campaign ID path parameter from the smsmode API route. |
| `messageId` | string | yes | Message ID path parameter from the smsmode API route. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native smsmode API returns.

## Native endpoint

Through the native smsmode API, this operation is `DELETE rcs/v1/channels/:channelId/campaigns/:campaignId/messages/:messageId` (base URL `https://rest.smsmode.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-scheduled-rcs-message.md) for the provider-specific parameters and requirements.

