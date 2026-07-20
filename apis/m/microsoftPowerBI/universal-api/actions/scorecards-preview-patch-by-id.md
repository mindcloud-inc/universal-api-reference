# Microsoft Power BI: Patch By ID



```
PUT https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/scorecards-preview-patch-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/scorecards-preview-patch-by-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupId": "string",
  "scorecardId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/scorecards-preview-patch-by-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupId": "string",
    "scorecardId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupId` | string | yes | The unique identifier of the workspace |
| `scorecardId` | string | yes | The unique identifier of the scorecard |
| `columnSettings[]` | array<object> | no | The display settings for columns on a scorecard |
| `createdTime` | date | no | The UTC time at creation |
| `datasetId` | string | no | The ID of the dataset associated with the scorecard |
| `description` | string | no | The scorecard description |
| `goals[]` | array<object> | no | The scorecard goals |
| `id` | string | no | The scorecard ID |
| `lastModifiedTime` | date | no | The UTC time at last modification |
| `name` | string | no | The scorecard name |
| `permissions` | object | no | The scorecard permissions |
| `provisioningStatus` | object | no | The provisioning status of the scorecard. |
| `reportId` | string | no | The ID of the internal report associated with the scorecard |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Power BI API returns.

## Native endpoint

Through the native Microsoft Power BI API, this operation is `PATCH groups/[:groupId]/scorecards([:scorecardId])` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/scorecards-preview-patch-by-id.md) for the provider-specific parameters and requirements.

