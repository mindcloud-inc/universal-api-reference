# Microsoft Power BI: List Dataset Refresh History in Workspace



```
GET https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/list-dataset-refresh-history-in-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/list-dataset-refresh-history-in-workspace?connectionId=$CONNECTION_ID&groupId=f089354e-8366-4e18-aea3-4cb4a3a50b48&datasetId=cfafbeb1-8037-4d0c-896e-a46fb27ff229" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupId": "f089354e-8366-4e18-aea3-4cb4a3a50b48",
  "datasetId": "cfafbeb1-8037-4d0c-896e-a46fb27ff229"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/list-dataset-refresh-history-in-workspace?${params}`, {
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
| `groupId` | string | yes | The Power BI workspace ID. Example: `f089354e-8366-4e18-aea3-4cb4a3a50b48`. |
| `datasetId` | string | yes | The Power BI dataset ID. Example: `cfafbeb1-8037-4d0c-896e-a46fb27ff229`. |
| `top` | number | no | The requested number of entries in the refresh history. If omitted, Power BI returns the last available 60 entries. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "endTime": "2026-05-07T12:00:00.000Z",
      "refreshAttempts": [
        {}
      ],
      "refreshType": "string",
      "requestId": "string",
      "serviceExceptionJson": "string",
      "startTime": "2026-05-07T12:00:00.000Z",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `endTime` | date | The refresh end time in UTC. |
| `refreshAttempts` | array<object> | Details for refresh attempts made by Power BI. |
| `refreshType` | string | The type of refresh request. |
| `requestId` | string | The identifier of the refresh request. |
| `serviceExceptionJson` | string | Failure error code JSON when the refresh failed. |
| `startTime` | date | The refresh start time in UTC. |
| `status` | string | The refresh status, such as Unknown, Completed, Failed, or Disabled. |

## Native endpoint

Through the native Microsoft Power BI API, this operation is `GET groups/[:groupId]/datasets/[:datasetId]/refreshes` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-dataset-refresh-history-in-workspace.md) for the provider-specific parameters and requirements.

