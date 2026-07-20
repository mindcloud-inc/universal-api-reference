# Microsoft Power BI: Clone Report



```
POST https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/reports-clone-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/reports-clone-report" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "reportId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/reports-clone-report', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "reportId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `reportId` | string | yes | The report ID |
| `name` | string | yes | The new report name |
| `targetModelId` | string | no | Optional. Parameter for specifying the target associated dataset ID. If not provided, the new report will be associated with the same dataset as the source report. |
| `targetWorkspaceId` | string | no | Optional. Parameter for specifying the target workspace ID. An empty GUID (00000000-0000-0000-0000-000000000000) indicates **My workspace**. If this parameter isn't provided, the new report will be cloned within the same workspace as the source report. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Power BI API returns.

## Native endpoint

Through the native Microsoft Power BI API, this operation is `POST reports/[:reportId]/Clone` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reports-clone-report.md) for the provider-specific parameters and requirements.

