# CallPage: Update SMS Message

Updates an existing SMS message in CallPage.

```
PUT https://connect.mindcloud.co/v1/universal/callPage/latest/actions/update-sms-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallPage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/callPage/latest/actions/update-sms-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "widgetId": 1,
  "messageId": "visitor.call-scheduled",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/callPage/latest/actions/update-sms-message', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "widgetId": 1,
    "messageId": "visitor.call-scheduled",
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `widgetId` | number | yes | The widget identifier. |
| `messageId` | list<string> | yes | The SMS message identifier. One of: `visitor.call-scheduled`, `visitor.cancel-scheduled`, `visitor.dial-completed`, `visitor.incoming-dial-completed`. |
| `enabled` | boolean | no | Whether the SMS should be enabled. Default: `true`. |
| `text` | string | yes | The SMS text. Maximum 240 characters. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | The updated custom SMS identifier. |

## Native endpoint

Through the native CallPage API, this operation is `POST /sms/update` (base URL `https://core.callpage.io/api/v1/external`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-sms-message.md) for the provider-specific parameters and requirements.

