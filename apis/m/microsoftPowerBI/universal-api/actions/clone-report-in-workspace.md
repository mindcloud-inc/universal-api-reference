# Microsoft Power BI: Clone Report in Workspace



```
POST https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/clone-report-in-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/clone-report-in-workspace" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupId": "string",
  "reportId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/clone-report-in-workspace', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupId": "string",
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
| `groupId` | string | yes | The source Power BI workspace ID. |
| `reportId` | string | yes | The report ID to clone. |
| `name` | string | yes | The name for the cloned report. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `targetWorkspaceId` | string | no | Optional target workspace ID for the cloned report. |
| `targetModelId` | string | no | Optional target dataset ID for the cloned report. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Power BI API returns.

## Native endpoint

Through the native Microsoft Power BI API, this operation is `POST groups/[:groupId]/reports/[:reportId]/Clone` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/clone-report-in-workspace.md) for the provider-specific parameters and requirements.

