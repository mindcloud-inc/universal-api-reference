# MojoTxt: Create Subscription List

Creates a subscription list in MojoTxt.

```
POST https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/create-subscription-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MojoTxt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/create-subscription-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "keyword": "string",
  "listName": "Ava Chen",
  "phoneNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/create-subscription-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "keyword": "string",
    "listName": "Ava Chen",
    "phoneNumber": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `keyword` | string | yes | The unique keyword for the subscription list. |
| `listName` | string | yes | The descriptive name of the subscription list. |
| `phoneNumber` | string | yes | The MojoTxt phone number in international format, like +17792533748. |
| `sendLastMessage` | number | no | Set to 1 to send the last sent message when someone joins the list. |
| `welcomeMessage` | string | no | Message sent to new subscribers when they join the list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_id": 1,
      "message": "string",
      "result": "string",
      "timestamp": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_id` | number | ID of the newly created subscription list. |
| `message` | string | Human-readable create result message. |
| `result` | string | Whether the create request succeeded. |
| `timestamp` | number | MojoTxt server timestamp for the response. |

## Native endpoint

Through the native MojoTxt API, this operation is `POST /:phoneNumber/lists/add` (base URL `https://app.mojotxt.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-subscription-list.md) for the provider-specific parameters and requirements.

