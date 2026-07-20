# Flow App: Get Event Summary CSV



```
GET https://connect.mindcloud.co/v1/universal/flowApp/latest/actions/get-event-summary-csv
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flow App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flowApp/latest/actions/get-event-summary-csv?connectionId=$CONNECTION_ID&sessionToken=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sessionToken": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flowApp/latest/actions/get-event-summary-csv?${params}`, {
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
| `sessionToken` | string | yes | The event session token for the compiled summary CSV report. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attendeeChat": "string",
      "operatorChat": "string",
      "registrants": "string",
      "surveyResults": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attendeeChat` | string | CSV data for attendee chat, matching the attendee chat CSV report. |
| `operatorChat` | string | CSV data for operator chat, matching the operator chat CSV report. |
| `registrants` | string | CSV data for registrants, matching the registrants CSV report. |
| `surveyResults` | string | Survey report data returned in Flow's compiled summary payload. |

## Native endpoint

Through the native Flow App API, this operation is `GET /reports/events/sessions/csv/summary/:sessionToken` (base URL `https://prod.flowapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event-summary-csv.md) for the provider-specific parameters and requirements.

