# Microsoft Power BI: Refresh Dataset



```
POST https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/datasets-refresh-dataset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/datasets-refresh-dataset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "datasetId": "string",
  "notifyOption": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/datasets-refresh-dataset', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "datasetId": "string",
    "notifyOption": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `datasetId` | string | yes | The dataset ID |
| `notifyOption` | object | yes | Mail notification options. This parameter is not applicable to enhanced refreshes or API operations with a service principal. |
| `applyRefreshPolicy` | boolean | no | Determine if the policy is applied or not |
| `commitMode` | object | no | Determines if objects will be committed in batches or only when complete |
| `effectiveDate` | date | no | If an incremental refresh policy is applied, the effectiveDate parameter overrides the current date. |
| `maxParallelism` | number | no | The maximum number of threads on which to run parallel processing commands |
| `objects[]` | array<object> | no | An array of objects to be processed |
| `retryCount` | number | no | Number of times the operation will retry before failing. Temporary internal errors may trigger a retry of the refresh, even when this parameter is set to 0. |
| `timeout` | string | no | 2[0-3]):[0-5][0-9]:[0-5][0-9]$ |
| `type` | object | no | The type of processing to perform |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Power BI API returns.

## Native endpoint

Through the native Microsoft Power BI API, this operation is `POST datasets/[:datasetId]/refreshes` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/datasets-refresh-dataset.md) for the provider-specific parameters and requirements.

