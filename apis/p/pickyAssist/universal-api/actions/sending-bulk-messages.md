# Picky Assist: Sending Bulk Messages



```
POST https://connect.mindcloud.co/v1/universal/pickyAssist/latest/actions/sending-bulk-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Picky Assist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pickyAssist/latest/actions/sending-bulk-messages" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "application": "string",
  "globalmessage": "string",
  "data[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pickyAssist/latest/actions/sending-bulk-messages', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "application": "string",
    "globalmessage": "string",
    "data[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `application` | string | yes | The channel/application id that should send the message. |
| `globalmessage` | string | yes | Shared message text used for all recipient rows in the bulk request. |
| `data[]` | array<object> | yes | Recipient rows for the bulk push request. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `priority` | string | no | Message priority value used by Picky Assist. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "credit": "string",
          "msg_id": "string",
          "number": "string"
        }
      ],
      "message": "string",
      "push_id": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].credit` | string |  |
| `data[].msg_id` | string |  |
| `data[].number` | string |  |
| `message` | string |  |
| `push_id` | string |  |
| `status` | number |  |

## Native endpoint

Through the native Picky Assist API, this operation is `POST /push` (base URL `https://app.pickyassist.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/sending-bulk-messages.md) for the provider-specific parameters and requirements.

