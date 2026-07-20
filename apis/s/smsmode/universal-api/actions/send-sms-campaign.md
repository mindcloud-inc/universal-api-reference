# smsmode: Send SMS Campaign



```
POST https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/send-sms-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a smsmode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/send-sms-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channelId": "string",
  "recipients[]": [
    "string"
  ],
  "body": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/send-sms-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channelId": "string",
    "recipients[]": ["string"],
    "body": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channelId` | string | yes | Channel ID path parameter from the smsmode API route. |
| `recipients[]` | array | yes | Recipients request body field documented by the smsmode API. |
| `body` | object | yes | Body request body field documented by the smsmode API. |
| `from` | string | no | Sender request body field documented by the smsmode API. |
| `sentDate` | date | no | Send Date request body field documented by the smsmode API. |
| `endDate` | date | no | End Date request body field documented by the smsmode API. |
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
      "endDate": "2026-05-07T12:00:00.000Z",
      "from": "string",
      "recipients": [
        {
          "refClient": "string",
          "to": "string"
        }
      ],
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
| `endDate` | date |  |
| `from` | string |  |
| `recipients[].refClient` | string |  |
| `recipients[].to` | string |  |
| `refClient` | string |  |
| `sentDate` | date |  |

## Native endpoint

Through the native smsmode API, this operation is `POST sms/v1/channels/:channelId/campaigns` (base URL `https://rest.smsmode.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-sms-campaign.md) for the provider-specific parameters and requirements.

