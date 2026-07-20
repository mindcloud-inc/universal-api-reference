# CallPage: Reset SMS Messages

Deletes all SMS messages from CallPage.

```
DELETE https://connect.mindcloud.co/v1/universal/callPage/latest/actions/reset-sms-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallPage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/callPage/latest/actions/reset-sms-messages?connectionId=$CONNECTION_ID&widgetId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "widgetId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callPage/latest/actions/reset-sms-messages?${params}`, {
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
| `widgetId` | number | yes | The widget identifier. |
| `messageId` | list<string> | no | The SMS message identifier. One of: `visitor.call-scheduled`, `visitor.cancel-scheduled`, `visitor.dial-completed`, `visitor.incoming-dial-completed`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CallPage API returns.

## Native endpoint

Through the native CallPage API, this operation is `POST /sms/reset` (base URL `https://core.callpage.io/api/v1/external`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reset-sms-messages.md) for the provider-specific parameters and requirements.

