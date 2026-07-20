# smsmode: Update Scheduled SMS Message



```
PUT https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/update-scheduled-sms-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a smsmode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/update-scheduled-sms-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channelId": "string",
  "campaignId": "string",
  "messageId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/update-scheduled-sms-message', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channelId": "string",
    "campaignId": "string",
    "messageId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channelId` | string | yes | Channel ID path parameter from the smsmode API route. |
| `campaignId` | string | yes | Campaign ID path parameter from the smsmode API route. |
| `messageId` | string | yes | Message ID path parameter from the smsmode API route. |
| `recipient` | object | no | Recipient request body field documented by the smsmode API. |
| `body` | object | no | Body request body field documented by the smsmode API. |
| `from` | string | no | Sender request body field documented by the smsmode API. |
| `sentDate` | date | no | Send Date request body field documented by the smsmode API. |
| `refClient` | string | no | Client Reference request body field documented by the smsmode API. |
| `callbackUrlStatus` | string | no | Status Callback URL request body field documented by the smsmode API. |
| `callbackUrlMo` | string | no | MO Callback URL request body field documented by the smsmode API. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": {
        "encoding": "string",
        "length": 1,
        "messagePartCount": 1,
        "stop": true,
        "text": "string"
      },
      "callbackUrlMo": "https://example.com",
      "callbackUrlStatus": "https://example.com",
      "from": "string",
      "recipient": {
        "to": "string"
      },
      "refClient": "string",
      "sentDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body.encoding` | string |  |
| `body.length` | number |  |
| `body.messagePartCount` | number |  |
| `body.stop` | boolean |  |
| `body.text` | string |  |
| `callbackUrlMo` | string |  |
| `callbackUrlStatus` | string |  |
| `from` | string |  |
| `recipient.to` | string |  |
| `refClient` | string |  |
| `sentDate` | date |  |

## Native endpoint

Through the native smsmode API, this operation is `PATCH sms/v1/channels/:channelId/campaigns/:campaignId/messages/:messageId` (base URL `https://rest.smsmode.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-scheduled-sms-message.md) for the provider-specific parameters and requirements.

