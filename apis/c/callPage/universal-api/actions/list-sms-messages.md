# CallPage: List SMS Messages

Retrieves all SMS messages from CallPage.

```
GET https://connect.mindcloud.co/v1/universal/callPage/latest/actions/list-sms-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallPage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callPage/latest/actions/list-sms-messages?connectionId=$CONNECTION_ID&widgetId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "widgetId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callPage/latest/actions/list-sms-messages?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "enabled": true,
      "message_id": "string",
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `enabled` | boolean | Whether the SMS is enabled. |
| `message_id` | string | The SMS message identifier. |
| `text` | string | The SMS text. |

## Native endpoint

Through the native CallPage API, this operation is `GET /sms/all` (base URL `https://core.callpage.io/api/v1/external`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sms-messages.md) for the provider-specific parameters and requirements.

