# SMS Connexion: Estimate SMS

Estimates a new SMS in SMS Connexion.

```
GET https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/estimate-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMS Connexion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/estimate-sms?connectionId=$CONNECTION_ID&to=string&from=string&text=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "to": "string",
  "from": "string",
  "text": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/estimate-sms?${params}`, {
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
| `to` | string | yes | Recipient phone number in E.164 format. |
| `from` | string | yes | Approved originator/sender ID. |
| `text` | string | yes | SMS message content. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignId": "string",
      "characters": [
        "string"
      ],
      "cost": 1,
      "countryIso": "string",
      "createdAt": "string",
      "data": [
        "string"
      ],
      "encoding": "string",
      "from": "string",
      "info": {},
      "inQuietHours": true,
      "invalid": [
        "string"
      ],
      "length": 1,
      "msgId": "string",
      "original": {},
      "parts": 1,
      "phoneNumbersByCountry": {},
      "replaced": {},
      "scheduled": true,
      "status": "string",
      "statusCode": 1,
      "text": {},
      "textAnalysis": {},
      "to": "string",
      "totalCost": 1,
      "totalCostSaved": 1,
      "totalInvalid": 1,
      "totalOriginalCost": 1,
      "totalOriginalParts": 1,
      "totalParts": 1,
      "totalPartsSaved": 1,
      "totalPhoneNumbers": 1,
      "totalReplacedCost": 1,
      "totalReplacedParts": 1,
      "totalValid": 1,
      "transliterationAnalysis": {},
      "unicode": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignId` | string |  |
| `characters` | array |  |
| `cost` | number |  |
| `countryIso` | string |  |
| `createdAt` | string |  |
| `data` | array |  |
| `encoding` | string |  |
| `from` | string |  |
| `info` | object |  |
| `inQuietHours` | boolean |  |
| `invalid` | array |  |
| `length` | number |  |
| `msgId` | string |  |
| `original` | object |  |
| `parts` | number |  |
| `phoneNumbersByCountry` | object |  |
| `replaced` | object |  |
| `scheduled` | boolean |  |
| `status` | string |  |
| `statusCode` | number |  |
| `text` | object |  |
| `textAnalysis` | object |  |
| `to` | string |  |
| `totalCost` | number |  |
| `totalCostSaved` | number |  |
| `totalInvalid` | number |  |
| `totalOriginalCost` | number |  |
| `totalOriginalParts` | number |  |
| `totalParts` | number |  |
| `totalPartsSaved` | number |  |
| `totalPhoneNumbers` | number |  |
| `totalReplacedCost` | number |  |
| `totalReplacedParts` | number |  |
| `totalValid` | number |  |
| `transliterationAnalysis` | object |  |
| `unicode` | boolean |  |

## Native endpoint

Through the native SMS Connexion API, this operation is `POST /sms/estimate` (base URL `https://api.sms.cx`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/estimate-sms.md) for the provider-specific parameters and requirements.

