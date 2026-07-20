# SMS Connexion: Get Advanced Report

Retrieves an advanced report from SMS Connexion.

```
GET https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/get-advanced-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMS Connexion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/get-advanced-report?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/get-advanced-report?${params}`, {
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
| `period` | string | no | Reporting period (YYYY-MM or YYYY). Example: `2026-03`. |
| `startDate` | string | no | Start date in YYYY-MM-DD. Example: `2026-03-01`. |
| `endDate` | string | no | End date in YYYY-MM-DD. Example: `2026-03-31`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channel": "string",
      "cost": 1,
      "countryIso": "string",
      "createdAt": "string",
      "data": [
        "string"
      ],
      "from": "string",
      "info": {},
      "inQuietHours": true,
      "length": 1,
      "msgId": "string",
      "parts": 1,
      "source": "string",
      "status": "string",
      "statusCode": 1,
      "text": "string",
      "textAnalysis": {},
      "to": "string",
      "totalCost": 1,
      "totalParts": 1,
      "totalPhoneNumbers": 1,
      "unicode": true,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channel` | string |  |
| `cost` | number |  |
| `countryIso` | string |  |
| `createdAt` | string |  |
| `data` | array |  |
| `from` | string |  |
| `info` | object |  |
| `inQuietHours` | boolean |  |
| `length` | number |  |
| `msgId` | string |  |
| `parts` | number |  |
| `source` | string |  |
| `status` | string |  |
| `statusCode` | number |  |
| `text` | string |  |
| `textAnalysis` | object |  |
| `to` | string |  |
| `totalCost` | number |  |
| `totalParts` | number |  |
| `totalPhoneNumbers` | number |  |
| `unicode` | boolean |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native SMS Connexion API, this operation is `GET /reports` (base URL `https://api.sms.cx`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-advanced-report.md) for the provider-specific parameters and requirements.

