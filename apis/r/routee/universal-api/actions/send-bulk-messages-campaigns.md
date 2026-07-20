# Routee: Send Bulk Messages - Campaigns

Sends bulk messages - campaigns with Routee.

```
POST https://connect.mindcloud.co/v1/universal/routee/latest/actions/send-bulk-messages-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/routee/latest/actions/send-bulk-messages-campaigns" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "from": "string",
  "body": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/routee/latest/actions/send-bulk-messages-campaigns', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "from": "string",
    "body": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contacts[]` | array<string> | no | The contact ids that the message will be sent to. Contacts have to be uploaded to the system. One of "groups", "to", "contacts" parameters is required. |
| `groups[]` | array<string> | no | The groups of contacts in the account selected as recipients. Groups have to be created at the system. One of "groups", "to", "contacts" parameters is required. |
| `to[]` | array<string> | no | The phone numbers (array) the message is about to be sent to. Format with a '+' and country code e.g., +306948530920 (E.164 format). Maximum array of number allowed 30k. One of "groups", "to", "contacts" parameters is required. |
| `from` | string | yes | The sender of the message. This can be a telephone number (numeric string with maximum length 16 characters) or an alphanumeric string (maximum length 11 characters). When you want to use a [number](/docs/numbers), you have to enter it without the '+' before the country code (eg 447123123456). |
| `body` | string | yes | The message you want to send. Use "\n" to create a new line in your message. Use [~{labelName}] in order to send personalized messages, by using the labels of your contacts. |
| `scheduledDate` | date | no | Defines the scheduled date and time in UTC. (eg YYYY-MM-DDThh:mm:ssTZD where TZD is the time zone designator (Z or +hh:mm or -hh:mm)) |
| `campaignName` | string | no | The name of the campaign. If you want to be able to track the whole campaign from Routee web platform use a name. If no name is provided you won’t be able to see the campaign from Routee web platform but you can track all the individual messages. Must be between 2 and 30 characters and contain only latin letters, numbers, spaces and - |
| `flash` | boolean | no | Indicates if the SMS is a flash SMS. A flash SMS is a type of SMS that appears directly on the main screen without user interaction and is not automatically stored in the inbox. It can be useful in emergencies, such as a fire alarm or cases of confidentiality, as in delivering one-time passwords. Default value false |
| `respectQuietHours` | boolean | no | Indicates if the SMS should respect the quiet hours. Quiet Hours are set by default to 23.00 - 08.00 and 14.00-17.00 destination local time. Please note that not all countries are supported with this feature due to multiple time zones within the country. Default value false |
| `campaignCallback` | object | no | Defines the notification callback information for the progress of the SMS campaign. Check [here](/docs/callbacks) for the payload information |
| `callback` | object | no | Defines the notification callback information for an individual message progress of the SMS campaign. Check [here](/docs/callbacks) for the payload information |
| `reminder` | object | no | Defines the recipients that will receive a test SMS before the actual SMS campaign is sent. |
| `fallbackValues` | string | no | Defines the default values when the SMS has labels, in case a contact does not contain any of these labels. |
| `ttl` | number | no | The duration in minutes the delivery of an SMS will be attempted. Must be between 1-4320. By default Routee will attempt delivery for 72 hours. If the SMS is not delivered within the validity period, then the SMS status will be "Undelivered", with "detailedStatus": "Expired" |
| `allowInvalid` | boolean | no | Allow invalid recipients. By setting 'allowInvalid' to true, the API will not return the invalid numbers and will sent the messages to the valid ones only |
| `urlShortener` | object | no | [OPTIONAL] If present, each link that exist in message body will be replaced by a Shortened URL. NOTE: Links are recognized by the prefix "http://" or "https://" and are separated by the next word or character with space. Keep in mind that adding any character like '.' ',' etc, other than space at the end of the link, will be recognized as part of the url and it will result to a shortened url that redirects to a wrong destination. |
| `restrictions` | object | no | [OPTIONAL] Provide the registered Content Template ID and Principal Entity ID to ensure the message is not rejected by TRAI regulations. |
| `transcode` | boolean | no | If “transcode” is set to true/false, then the message body will be/not be transcoded. If the “transcode” parameter is not set, then the application level setting will be used. In case the message can be sent as UTF in one part, it will not be transcoded. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": "string",
      "cost": 1,
      "createdAt": "string",
      "flash": true,
      "from": "string",
      "respectQuietHours": true,
      "smsAnalysis": {
        "bodyAnalysis": {
          "characters": 1,
          "parts": 1,
          "unicode": true
        },
        "contacts": {},
        "numberOfRecipients": 1,
        "recipientCountries": {
          "+30693xxxxxxx": "string",
          "+30694xxxxxxx": "string",
          "+30697xxxxxxx": "string"
        },
        "recipientsPerCountry": {
          "GR": 1
        },
        "recipientsPerGroup": {},
        "totalInGroups": 1
      },
      "state": "string",
      "statuses": {
        "Delivered": 1,
        "Failed": 1,
        "Queued": 1,
        "Sent": 1,
        "Undelivered": 1,
        "Unsent": 1
      },
      "to": [
        [
          "string"
        ]
      ],
      "totalMessages": 1,
      "trackingId": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | string |  |
| `cost` | number |  |
| `createdAt` | string |  |
| `flash` | boolean |  |
| `from` | string |  |
| `respectQuietHours` | boolean |  |
| `smsAnalysis` | object |  |
| `smsAnalysis.bodyAnalysis` | object |  |
| `smsAnalysis.bodyAnalysis.characters` | number |  |
| `smsAnalysis.bodyAnalysis.parts` | number |  |
| `smsAnalysis.bodyAnalysis.unicode` | boolean |  |
| `smsAnalysis.contacts` | object |  |
| `smsAnalysis.numberOfRecipients` | number |  |
| `smsAnalysis.recipientCountries` | object |  |
| `smsAnalysis.recipientCountries.+30693xxxxxxx` | string |  |
| `smsAnalysis.recipientCountries.+30694xxxxxxx` | string |  |
| `smsAnalysis.recipientCountries.+30697xxxxxxx` | string |  |
| `smsAnalysis.recipientsPerCountry` | object |  |
| `smsAnalysis.recipientsPerCountry.GR` | number |  |
| `smsAnalysis.recipientsPerGroup` | object |  |
| `smsAnalysis.totalInGroups` | number |  |
| `state` | string |  |
| `statuses` | object |  |
| `statuses.Delivered` | number |  |
| `statuses.Failed` | number |  |
| `statuses.Queued` | number |  |
| `statuses.Sent` | number |  |
| `statuses.Undelivered` | number |  |
| `statuses.Unsent` | number |  |
| `to[]` | array<string> |  |
| `totalMessages` | number |  |
| `trackingId` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Routee API, this operation is `POST /sms/campaign` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-bulk-messages-campaigns.md) for the provider-specific parameters and requirements.

