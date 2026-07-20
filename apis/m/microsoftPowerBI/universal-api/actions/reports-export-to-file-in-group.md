# Microsoft Power BI: Export To File In Group



```
POST https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/reports-export-to-file-in-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/reports-export-to-file-in-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupId": "string",
  "reportId": "string",
  "format": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/reports-export-to-file-in-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupId": "string",
    "reportId": "string",
    "format": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupId` | string | yes | The workspace ID |
| `reportId` | string | yes | The report ID |
| `format` | object | yes | The requested format for the exported file |
| `paginatedReportConfiguration` | object | no | The configuration used to export a paginated report |
| `powerBIReportConfiguration` | object | no | The configuration used to export a Power BI report |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Power BI API returns.

## Native endpoint

Through the native Microsoft Power BI API, this operation is `POST groups/[:groupId]/reports/[:reportId]/ExportTo` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reports-export-to-file-in-group.md) for the provider-specific parameters and requirements.

