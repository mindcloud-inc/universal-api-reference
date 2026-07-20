# CallRail: Summarize Call Data

Retrieves call summary data from CallRail.

```
GET https://connect.mindcloud.co/v1/universal/callRail/latest/actions/summarize-call-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallRail `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callRail/latest/actions/summarize-call-data?connectionId=$CONNECTION_ID&account_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "account_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callRail/latest/actions/summarize-call-data?${params}`, {
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
| `account_id` | string | yes | The CallRail account ID. |
| `company_id` | string | no | Limit the summary to one company. |
| `group_by` | string | no | Group summary results by a supported dimension. |
| `fields` | string | no | Comma-separated summary fields to include. |
| `answer_status` | string | no | Filter by whether calls were answered or missed. |
| `first_time_callers` | boolean | no | Restrict results to first-time callers when true. |
| `lead_status` | string | no | Filter summary results by lead status. |
| `agent` | string | no | Limit the summary to calls attributed to a specific agent. |
| `date_range` | string | no | Standard CallRail date range filter. |
| `start_date` | string | no | Start of a custom date range in ISO 8601 format. |
| `end_date` | string | no | End of a custom date range in ISO 8601 format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "endDate": "string",
      "startDate": "string",
      "timeZone": "string",
      "totalResults": {
        "answeredCalls": 1,
        "totalCalls": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `endDate` | string |  |
| `startDate` | string |  |
| `timeZone` | string |  |
| `totalResults` | object |  |
| `totalResults.answeredCalls` | number |  |
| `totalResults.totalCalls` | number |  |

## Native endpoint

Through the native CallRail API, this operation is `GET /v3/a/:account_id/calls/summary.json` (base URL `https://api.callrail.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/summarize-call-data.md) for the provider-specific parameters and requirements.

