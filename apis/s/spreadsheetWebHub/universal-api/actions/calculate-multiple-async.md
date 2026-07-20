# SpreadsheetWeb Hub: Calculate Multiple Async

Performs multiple asynchronous calculations in SpreadsheetWeb Hub.

```
GET https://connect.mindcloud.co/v1/universal/spreadsheetWebHub/latest/actions/calculate-multiple-async
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SpreadsheetWeb Hub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spreadsheetWebHub/latest/actions/calculate-multiple-async?connectionId=$CONNECTION_ID&request.applicationId=string&request.workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "request.applicationId": "string",
  "request.workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spreadsheetWebHub/latest/actions/calculate-multiple-async?${params}`, {
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
| `request.applicationId` | string | yes | SpreadsheetWeb application identifier for the async bulk calculation request. |
| `request.workspaceId` | string | yes | Workspace identifier for the async bulk calculation request. |
| `request.inputs` | object | no | Dictionary of calculation inputs keyed by request item identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string |  |

## Native endpoint

Through the native SpreadsheetWeb Hub API, this operation is `POST /calculations/calculatemultipleasync` (base URL `https://api.spreadsheetweb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/calculate-multiple-async.md) for the provider-specific parameters and requirements.

