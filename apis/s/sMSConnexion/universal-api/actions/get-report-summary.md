# SMS Connexion: Get Report Summary

Retrieves summary reports by dimension from SMS Connexion.

```
GET https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/get-report-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMS Connexion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/get-report-summary?connectionId=$CONNECTION_ID&dimension=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dimension": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/get-report-summary?${params}`, {
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
| `dimension` | string | yes | Summary dimension. Accepted values: source, channel, country, traffic, delivery. |
| `period` | string | no | Reporting period (YYYY-MM or YYYY). |
| `startDate` | string | no | Start date in YYYY-MM-DD. |
| `endDate` | string | no | End date in YYYY-MM-DD. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alerts": {},
      "api": {},
      "campaigns": {},
      "costParts": 1,
      "data": {},
      "parts": 1,
      "phoneNumbers": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alerts` | object |  |
| `api` | object |  |
| `campaigns` | object |  |
| `costParts` | number |  |
| `data` | object |  |
| `parts` | number |  |
| `phoneNumbers` | number |  |

## Native endpoint

Through the native SMS Connexion API, this operation is `GET /reports/summary/:dimension` (base URL `https://api.sms.cx`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-report-summary.md) for the provider-specific parameters and requirements.

