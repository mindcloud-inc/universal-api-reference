# Routee: Send a Voice Campaign

Sends a voice campaign with Routee.

```
POST https://connect.mindcloud.co/v1/universal/routee/latest/actions/send-a-voice-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/routee/latest/actions/send-a-voice-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "from": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/routee/latest/actions/send-a-voice-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "from": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `from` | string | yes | The sender id for this call. The sender id can be a telephone number or an alphanumeric string. NOTICE: Alphanumeric sender is not supported by all networks (e.g. Greek networks). Check restrictions and features here: https://go.routee.net/#/management/restrictions-and-features |
| `to[]` | array<string> | no | The recipients of this call, must be a list with valid numbers (mobiles or landlines). Max length: 1000. One of "groups", "to", "contacts" parameters are required. |
| `contacts[]` | array<string> | no | The contacts of this call, must be a list with valid contact ids. Max length: 1000. One of "groups", "to", "contacts" parameters are required. |
| `groups[]` | array<string> | no | The lists of this call, must be a list with valid group names. Max length: 1000. One of "groups", "to", "contacts" parameters are required. |
| `name` | string | no | The name of the voice campaign. The name of the campaign. If you want to be able to track the whole campaign from Routee web platform use a name. Must be between 2 and 30 characters and contain only latin letters, numbers, spaces and - |
| `fileURL` | string | no | The url of the wav file to play. One of fileURL or message parameters is required. |
| `message` | object | no | Represents the text message to be converted to speech. One of fileURL or message parameters is required. |
| `message.gender` | string | no | The gender of the voice message to be played. Check [here](/docs/text-to-speech) for possible values |
| `message.language` | string | no | The language of the voice message to be played. Check [here](/docs/text-to-speech) for possible values |
| `message.text` | string | no | The text of the voice message to be played |
| `respectQuietHours` | boolean | no | Indicates if the call should respect the quiet hours, default value: false. |
| `ignoreDnd` | boolean | no | Use this option when sending transactional messages. By enabling this option, Routee will ignore any Do Not Disturb list and will send the campaign to all the recipients you have provided. This option may violate user privacy. |
| `scheduledDate` | date | no | The date and time (in UTC), that the call campaign will be executed at. (eg YYYY-MM-DDThh:mm:ssTZD where TZD is the time zone designator (Z or +hh:mm or -hh:mm)) |
| `hangupDelay` | number | no | The time to wait for the call to be answered |
| `campaignCallback` | object | no | Information about a DLR callback for the progress of the Voice campaign. |
| `callback` | object | no | Defines the notification callback information for an individual message progress of the Voice campaign |
| `collectDtmfDigits` | boolean | no | Indicates if the voice campaign should collect DTMF digits at the end of the voice message. |
| `collectDtmfAwaitSeconds` | number | no | If you enable the collectDtmfDigits you can set the duration of the pause that will be added at the end of the voice message. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contacts": [
        [
          "string"
        ]
      ],
      "cost": 1,
      "createdAt": "string",
      "from": "string",
      "groups": [
        [
          "string"
        ]
      ],
      "message": {
        "gender": "string",
        "language": "string",
        "text": "string"
      },
      "respectQuietHours": true,
      "state": "string",
      "statuses": {
        "Busy": 1,
        "Completed": 1,
        "Failed": 1,
        "Initiated": 1,
        "InProgress": 1,
        "NoAnswer": 1,
        "Queued": 1,
        "Ringing": 1,
        "Terminated": 1,
        "Unknown": 1,
        "Unsent": 1
      },
      "to": [
        [
          "string"
        ]
      ],
      "trackingId": "string",
      "type": "string",
      "voiceAnalysis": {
        "contacts": {},
        "numberOfRecipients": 1,
        "recipientCountries": {
          "+306977663000": "string"
        },
        "recipientsPerCountry": {
          "GR": 1
        },
        "recipientsPerGroup": {},
        "totalInGroups": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contacts[]` | array |  |
| `cost` | number |  |
| `createdAt` | string |  |
| `from` | string |  |
| `groups[]` | array |  |
| `message` | object |  |
| `message.gender` | string |  |
| `message.language` | string |  |
| `message.text` | string |  |
| `respectQuietHours` | boolean |  |
| `state` | string |  |
| `statuses` | object |  |
| `statuses.Busy` | number |  |
| `statuses.Completed` | number |  |
| `statuses.Failed` | number |  |
| `statuses.Initiated` | number |  |
| `statuses.InProgress` | number |  |
| `statuses.NoAnswer` | number |  |
| `statuses.Queued` | number |  |
| `statuses.Ringing` | number |  |
| `statuses.Terminated` | number |  |
| `statuses.Unknown` | number |  |
| `statuses.Unsent` | number |  |
| `to[]` | array<string> |  |
| `trackingId` | string |  |
| `type` | string |  |
| `voiceAnalysis` | object |  |
| `voiceAnalysis.contacts` | object |  |
| `voiceAnalysis.numberOfRecipients` | number |  |
| `voiceAnalysis.recipientCountries` | object |  |
| `voiceAnalysis.recipientCountries.+306977663000` | string |  |
| `voiceAnalysis.recipientsPerCountry` | object |  |
| `voiceAnalysis.recipientsPerCountry.GR` | number |  |
| `voiceAnalysis.recipientsPerGroup` | object |  |
| `voiceAnalysis.totalInGroups` | number |  |

## Native endpoint

Through the native Routee API, this operation is `POST /voice/campaign` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-a-voice-campaign.md) for the provider-specific parameters and requirements.

