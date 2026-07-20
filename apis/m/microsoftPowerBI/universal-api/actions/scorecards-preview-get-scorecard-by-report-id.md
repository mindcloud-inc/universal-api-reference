# Microsoft Power BI: Get Scorecard By Report Id



```
GET https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/scorecards-preview-get-scorecard-by-report-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/scorecards-preview-get-scorecard-by-report-id?connectionId=$CONNECTION_ID&groupId=string&reportId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupId": "string",
  "reportId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/scorecards-preview-get-scorecard-by-report-id?${params}`, {
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
| `groupId` | string | yes | The unique identifier of the workspace |
| `reportId` | string | yes | The ID of the internal report associated with the scorecard |
| `_expand` | string | no | Accepts a comma-separated list of data types, which will be expanded inline in the response. Supports goals, goalValues, and aggregations. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Power BI API returns.

## Native endpoint

Through the native Microsoft Power BI API, this operation is `GET groups/[:groupId]/scorecards/GetScorecardByReportId(reportId=[:reportId])` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/scorecards-preview-get-scorecard-by-report-id.md) for the provider-specific parameters and requirements.

