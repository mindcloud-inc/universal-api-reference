# Microsoft Power BI: Update Datasources



```
POST https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/reports-update-datasources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/reports-update-datasources" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "reportId": "string",
  "updateDetails[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/reports-update-datasources', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "reportId": "string",
    "updateDetails[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `reportId` | string | yes | The report ID |
| `updateDetails[]` | array<object> | yes | The update details for the data sources of the paginated report |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Power BI API returns.

## Native endpoint

Through the native Microsoft Power BI API, this operation is `POST reports/[:reportId]/Default.UpdateDatasources` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reports-update-datasources.md) for the provider-specific parameters and requirements.

