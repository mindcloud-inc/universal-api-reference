# Microsoft Power BI: Refresh Dataset in Workspace



```
POST https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/refresh-dataset-in-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/refresh-dataset-in-workspace" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupId": "f089354e-8366-4e18-aea3-4cb4a3a50b48",
  "datasetId": "cfafbeb1-8037-4d0c-896e-a46fb27ff229"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/refresh-dataset-in-workspace', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupId": "f089354e-8366-4e18-aea3-4cb4a3a50b48",
    "datasetId": "cfafbeb1-8037-4d0c-896e-a46fb27ff229"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupId` | string | yes | The Power BI workspace ID. Example: `f089354e-8366-4e18-aea3-4cb4a3a50b48`. |
| `datasetId` | string | yes | The Power BI dataset ID. Example: `cfafbeb1-8037-4d0c-896e-a46fb27ff229`. |
| `notifyOption` | list | no | Mail notification option for the refresh request. One of: `0`, `1`, `2`. Default: `MailOnFailure`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Power BI API returns.

## Native endpoint

Through the native Microsoft Power BI API, this operation is `POST groups/[:groupId]/datasets/[:datasetId]/refreshes` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/refresh-dataset-in-workspace.md) for the provider-specific parameters and requirements.

