# Microsoft Power BI: Selective Deploy



```
POST https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/pipelines-selective-deploy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/pipelines-selective-deploy" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pipelineId": "string",
  "sourceStageOrder": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/pipelines-selective-deploy', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pipelineId": "string",
    "sourceStageOrder": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pipelineId` | string | yes | The deployment pipeline ID |
| `sourceStageOrder` | number | yes | The numeric identifier of the pipeline deployment stage that the content should be deployed from. Development (0), Test (1), Production (2). |
| `dashboards[]` | array<object> | no | A list of dashboards to be deployed |
| `dataflows[]` | array<object> | no | A list of dataflows to be deployed |
| `datamarts[]` | array<object> | no | A list of datamarts to be deployed |
| `datasets[]` | array<object> | no | A list of datasets to be deployed |
| `isBackwardDeployment` | boolean | no | Whether the deployment will be from a later stage in the deployment pipeline, to an earlier one. The default value is false. |
| `newWorkspace` | object | no | The configuration details for creating a new workspace. Required when deploying to a stage that has no assigned workspaces. The deployment will fail if the new workspace configuration details aren't provided when required. |
| `note` | string | no | A note describing the deployment. |
| `options` | object | no | Options that control the behavior of the entire deployment |
| `reports[]` | array<object> | no | A list of reports to be deployed |
| `updateAppSettings` | date | no | Update org app in the target workspace settings |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Power BI API returns.

## Native endpoint

Through the native Microsoft Power BI API, this operation is `POST pipelines/[:pipelineId]/deploy` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/pipelines-selective-deploy.md) for the provider-specific parameters and requirements.

