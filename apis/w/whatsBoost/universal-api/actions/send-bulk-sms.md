# WhatsBoost: Send Bulk SMS

Sends bulk SMS messages from WhatsBoost.

```
POST https://connect.mindcloud.co/v1/universal/whatsBoost/latest/actions/send-bulk-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhatsBoost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/whatsBoost/latest/actions/send-bulk-sms" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mode": "string",
  "campaign": "string",
  "message": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/whatsBoost/latest/actions/send-bulk-sms', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mode": "string",
    "campaign": "string",
    "message": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mode` | string | yes | Mode of sending the message, it can be 'devices' which will allow you to use your linked android devices or 'credits' which will allow you to use gateways and partner devices. 'credits' requires you to have enough credit balance to send messages. |
| `campaign` | string | yes | Name of the campaign, you will see this in the SMS campaign manager. |
| `numbers` | string | no | List of phone numbers separated by commas. It can be optional if 'groups' parameter is not empty. It will accept E.164 formatted numbers or locally formatted numbers using the country code from your profile settings. E.164: +34612345678 Local: 612345678. |
| `groups` | string | no | List of contact group ID's separated by commas. It can be optional if 'numbers' parameter is not empty. You can get group ID's from /get/groups (Your contact groups). |
| `message` | string | yes | Message you want to send, spintax and shortcodes are supported. |
| `device` | string | no | Linked device unique ID, this is required if you will send with 'devices' mode. You can get linked device unique ID from /get/devices (Your devices). |
| `gateway` | string | no | Partner device unique ID or gateway ID, this is required if you will send with 'credits' mode. You can get a partner device unique ID and gateway ID from /get/rates. |
| `sim` | number | no | SIM slot number you want to use. For 'devices' mode only. |
| `priority` | number | no | Priority level. 0 or 1 = high priority (sent immediately), 2 = normal priority (queued). For 'devices' mode only. |
| `shortener` | number | no | Shortener ID, specify the shortener you want to use if you want to shorten the links in your message. You can get the list of available shorteners from /get/shorteners. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `message` | string |  |
| `status` | number |  |

## Native endpoint

Through the native WhatsBoost API, this operation is `POST /send/sms.bulk` (base URL `https://whatsboost.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-bulk-sms.md) for the provider-specific parameters and requirements.

