# SMS Connexion: Get Campaign Report

Retrieves a campaign report from SMS Connexion.

```
GET https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/get-campaign-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMS Connexion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/get-campaign-report?connectionId=$CONNECTION_ID&campaignId=cbf5c28e-2db9-4f7c-9d1d-7e4a64dfec9a" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "cbf5c28e-2db9-4f7c-9d1d-7e4a64dfec9a"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/get-campaign-report?${params}`, {
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
| `campaignId` | string | yes | Campaign UUID from report campaigns endpoints. Example: `cbf5c28e-2db9-4f7c-9d1d-7e4a64dfec9a`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignId": "string",
      "campaignName": "Ava Chen",
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
| `campaignName` | string |  |
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

## Native endpoint

Through the native SMS Connexion API, this operation is `GET /reports/campaigns/:campaignId` (base URL `https://api.sms.cx`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign-report.md) for the provider-specific parameters and requirements.

