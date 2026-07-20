# SMS Connexion: Get Campaign Report XLSX Export

Retrieves a campaign report export from SMS Connexion as XLSX.

```
GET https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/get-campaign-report-xlsx-export
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMS Connexion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/get-campaign-report-xlsx-export?connectionId=$CONNECTION_ID&campaignId=cbf5c28e-2db9-4f7c-9d1d-7e4a64dfec9a" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "cbf5c28e-2db9-4f7c-9d1d-7e4a64dfec9a"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/get-campaign-report-xlsx-export?${params}`, {
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

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SMS Connexion API returns.

## Native endpoint

Through the native SMS Connexion API, this operation is `GET /reports/campaigns/:campaignId/xlsx` (base URL `https://api.sms.cx`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign-report-xlsx-export.md) for the provider-specific parameters and requirements.

