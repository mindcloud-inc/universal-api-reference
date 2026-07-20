# MojoTxt: Update Subscription List

Updates a subscription list in MojoTxt.

```
PUT https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/update-subscription-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MojoTxt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/update-subscription-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listIdOrKeyword": "string",
  "phoneNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/update-subscription-list', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listIdOrKeyword": "string",
    "phoneNumber": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `listIdOrKeyword` | string | yes | The subscription list identifier or keyword value to update. |
| `listName` | string | no | The updated descriptive name of the subscription list. |
| `phoneNumber` | string | yes | The MojoTxt phone number in international format, like +17792533748. |
| `sendLastMessage` | number | no | Set to 1 to send the last sent message when someone joins the list. |
| `welcomeMessage` | string | no | Message sent to new subscribers when they join the list. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
| `message` | string | Human-readable update result message. |
| `result` | string | Whether the update request succeeded. |
| `timestamp` | number | MojoTxt server timestamp for the response. |

## Native endpoint

Through the native MojoTxt API, this operation is `POST /:phoneNumber/lists/update/:listIdOrKeyword` (base URL `https://app.mojotxt.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-subscription-list.md) for the provider-specific parameters and requirements.

