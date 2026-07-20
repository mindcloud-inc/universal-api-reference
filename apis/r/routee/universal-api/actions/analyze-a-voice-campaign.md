# Routee: Analyze a Voice Campaign

Analyzes a voice campaign in Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/analyze-a-voice-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/analyze-a-voice-campaign?connectionId=$CONNECTION_ID&from=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "from": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/analyze-a-voice-campaign?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `from` | string | yes | The sender id for this call |
| `groups[]` | array<string> | no | The groups of contacts selected as recipients of this call. One of "groups", "to", "contacts" parameters is required. |
| `contacts[]` | array<string> | no | The contacts selected as recipients of this call. One of "groups", "to", "contacts" parameters is required. |
| `to[]` | array<string> | no | The recipients of this call, must be a list with valid numbers (mobiles or landlines). One of "groups", "to", "contacts" parameters is required. |
| `fileURL` | string | no | The url of the wav file to play |
| `message` | object | no | Represents the text message to be converted to wav file |
| `message.gender` | string | no | The gender of the voice message to be played |
| `message.language` | string | no | The language of the voice message to be played |
| `message.text` | string | no | The text of the voice message to be played |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contacts": {},
      "numberOfRecipients": 1,
      "recipientCountries": {
        "+306977663127": "string",
        "+447123123456": "string"
      },
      "recipientsPerCountry": {
        "GB": 1,
        "GR": 1
      },
      "recipientsPerGroup": {},
      "totalInGroups": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contacts` | object |  |
| `numberOfRecipients` | number |  |
| `recipientCountries` | object |  |
| `recipientCountries.+306977663127` | string |  |
| `recipientCountries.+447123123456` | string |  |
| `recipientsPerCountry` | object |  |
| `recipientsPerCountry.GB` | number |  |
| `recipientsPerCountry.GR` | number |  |
| `recipientsPerGroup` | object |  |
| `totalInGroups` | number |  |

## Native endpoint

Through the native Routee API, this operation is `POST /voice/analysis` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/analyze-a-voice-campaign.md) for the provider-specific parameters and requirements.

