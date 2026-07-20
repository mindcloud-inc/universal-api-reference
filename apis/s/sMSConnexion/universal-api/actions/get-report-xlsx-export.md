# SMS Connexion: Get Report XLSX Export

Retrieves an advanced report export from SMS Connexion as XLSX.

```
GET https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/get-report-xlsx-export
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMS Connexion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/get-report-xlsx-export?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/get-report-xlsx-export?${params}`, {
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
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native SMS Connexion API, this operation is `GET /reports/xlsx` (base URL `https://api.sms.cx`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-report-xlsx-export.md) for the provider-specific parameters and requirements.

