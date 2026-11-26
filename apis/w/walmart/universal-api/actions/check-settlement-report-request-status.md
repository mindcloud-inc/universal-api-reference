# Walmart: Check Settlement Report Request Status

Status values: RECEIVED, INPROGRESS, READY, ERROR.

```
GET https://connect.mindcloud.co/v1/universal/walmart/latest/actions/check-settlement-report-request-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/check-settlement-report-request-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/walmart/latest/actions/check-settlement-report-request-status?${params}`, {
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
| `requestId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channelType": "string",
      "payload": {
        "dataEndTime": "string",
        "dataStartTime": "string"
      },
      "reportGenerationDate": "string",
      "reportSummary": "string",
      "reportType": "string",
      "reportVersion": "string",
      "requestId": "string",
      "requestStatus": "string",
      "requestSubmissionDate": "string",
      "src": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channelType` | string |  |
| `payload.dataEndTime` | string |  |
| `payload.dataStartTime` | string |  |
| `reportGenerationDate` | string |  |
| `reportSummary` | string |  |
| `reportType` | string |  |
| `reportVersion` | string |  |
| `requestId` | string |  |
| `requestStatus` | string |  |
| `requestSubmissionDate` | string |  |
| `src` | string |  |

## Native endpoint

Through the native Walmart API, this operation is `GET https://marketplace.walmartapis.com/v3/reports/reportRequests/:requestId` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-settlement-report-request-status.md) for the provider-specific parameters and requirements.

