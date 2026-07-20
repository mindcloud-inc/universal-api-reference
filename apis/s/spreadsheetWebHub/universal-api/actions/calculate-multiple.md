# SpreadsheetWeb Hub: Calculate Multiple

Performs multiple calculations in SpreadsheetWeb Hub.

```
GET https://connect.mindcloud.co/v1/universal/spreadsheetWebHub/latest/actions/calculate-multiple
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SpreadsheetWeb Hub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spreadsheetWebHub/latest/actions/calculate-multiple?connectionId=$CONNECTION_ID&request.applicationId=string&request.workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "request.applicationId": "string",
  "request.workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spreadsheetWebHub/latest/actions/calculate-multiple?${params}`, {
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
| `request.applicationId` | string | yes | SpreadsheetWeb application identifier for the bulk calculation request. |
| `request.workspaceId` | string | yes | Workspace identifier for the bulk calculation request. |
| `request.inputs` | object | no | Dictionary of calculation inputs keyed by request item identifier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SpreadsheetWeb Hub API returns.

## Native endpoint

Through the native SpreadsheetWeb Hub API, this operation is `POST /calculations/calculatemultiple` (base URL `https://api.spreadsheetweb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/calculate-multiple.md) for the provider-specific parameters and requirements.

