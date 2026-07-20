# Routee: Send an SMS

Sends an SMS message with Routee.

```
POST https://connect.mindcloud.co/v1/universal/routee/latest/actions/send-an-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/routee/latest/actions/send-an-sms" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "from": "string",
  "body": "string",
  "to": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/routee/latest/actions/send-an-sms', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "from": "string",
    "body": "string",
    "to": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `from` | string | yes | The sender of the message. This can be a telephone number (numeric string with maximum length 16 characters) or an alphanumeric string (maximum length of 11 characters). When you want to use a [number](/docs/numbers), you have to enter it without the '+' before the country code (eg 447123123456). |
| `body` | string | yes | The message you want to send. Use "\n" to create a new line in your message. |
| `to` | string | yes | The destination phone number. Format with a '+' and country code e.g., +3069485xxxxx (E.164 format). |
| `flash` | boolean | no | Indicates if the SMS is a flash SMS. A flash SMS is a type of SMS that appears directly on the main screen without user interaction and is not automatically stored in the inbox. It can be useful in emergencies, such as a fire alarm or cases of confidentiality, as in delivering one-time passwords. Default value false. |
| `label` | string | no | A generic label which can be used for tagging the SMS. The maximum length is 350 characters. |
| `callback` | object | no | Defines the callback information for an individual message. Check [here](/docs/callbacks) for payload information. You can also set this value from Routee [Platform](https://go.routee.net/#/management/applications) on the Applications menu. |
| `ttl` | number | no | The duration in minutes the delivery of an SMS will be attempted. Must be between 1-4320. By default Routee will attempt delivery for 72 hours. If the SMS is not delivered within the validity period, then the SMS status will be "Undelivered", with "detailedStatus": "Expired". |
| `transcode` | boolean | no | If “transcode” is set to true/false, then the message body will be/not be transcoded. If the “transcode” parameter is not set, then the application level setting will be used. In case the message can be sent as UTF in one part, it will not be transcoded. |
| `urlShortener` | object | no | [OPTIONAL] If present, each link that exist in message body will be replaced by a Shortened URL. NOTE: Links are recognized by the prefix "http://" or "https://" and are separated by the next word or character with space. Keep in mind that adding any character like '.' ',' etc, other than space at the end of the link, will be recognized as part of the url and it will result to a shortened url that redirects to a wrong destination. |
| `restrictions` | object | no | [OPTIONAL] Provide the registered Content Template ID and Principal Entity ID to ensure the message is not rejected by TRAI regulations. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": "string",
      "bodyAnalysis": {
        "characters": 1,
        "parts": 1,
        "unicode": true
      },
      "createdAt": "string",
      "flash": true,
      "from": "string",
      "status": "string",
      "to": "string",
      "trackingId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | string |  |
| `bodyAnalysis` | object |  |
| `bodyAnalysis.characters` | number |  |
| `bodyAnalysis.parts` | number |  |
| `bodyAnalysis.unicode` | boolean |  |
| `createdAt` | string |  |
| `flash` | boolean |  |
| `from` | string |  |
| `status` | string |  |
| `to` | string |  |
| `trackingId` | string |  |

## Native endpoint

Through the native Routee API, this operation is `POST /sms` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-an-sms.md) for the provider-specific parameters and requirements.

