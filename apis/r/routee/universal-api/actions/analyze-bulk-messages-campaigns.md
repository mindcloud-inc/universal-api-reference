# Routee: Analyze Bulk Messages - Campaigns

Analyzes bulk message campaigns in Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/analyze-bulk-messages-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/analyze-bulk-messages-campaigns?connectionId=$CONNECTION_ID&from=string&body=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "from": "string",
  "body": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/analyze-bulk-messages-campaigns?${params}`, {
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
| `contacts[]` | array<string> | no | The contact ids that the message will be sent to. At least one of "contacts", "groups" or "to" is required. |
| `groups[]` | array<string> | no | The groups of contacts in the account selected as recipients. |
| `to[]` | array<string> | no | The phone numbers the message is about to be sent to. Format with a '+' and country code e.g., +306948530920 (E.164 format). |
| `from` | string | yes | The sender of the message. This can be a telephone number (numeric string with maximum length 16 characters) or an alphanumeric string (maximum length 11 characters). When you want to use a [number](/docs/numbers), you have to enter it without the '+' before the country code (eg 447123123456). |
| `body` | string | yes | The message you want to send. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
        "DE": 1,
        "FR": 1,
        "GR": 1,
        "RU": 1
      },
      "recipientsPerGroup": {
        "customers": 1
      },
      "totalInGroups": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bodyAnalysis` | object |  |
| `bodyAnalysis.characters` | number |  |
| `bodyAnalysis.parts` | number |  |
| `bodyAnalysis.unicode` | boolean |  |
| `contacts` | object |  |
| `numberOfRecipients` | number |  |
| `recipientCountries` | object |  |
| `recipientCountries.+30693xxxxxxx` | string |  |
| `recipientCountries.+30694xxxxxxx` | string |  |
| `recipientCountries.+30697xxxxxxx` | string |  |
| `recipientsPerCountry` | object |  |
| `recipientsPerCountry.DE` | number |  |
| `recipientsPerCountry.FR` | number |  |
| `recipientsPerCountry.GR` | number |  |
| `recipientsPerCountry.RU` | number |  |
| `recipientsPerGroup` | object |  |
| `recipientsPerGroup.customers` | number |  |
| `totalInGroups` | number |  |

## Native endpoint

Through the native Routee API, this operation is `POST /sms/analyze/campaign` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/analyze-bulk-messages-campaigns.md) for the provider-specific parameters and requirements.

