# MerrenIO: View Individual Table And Pie Chart Responses



```
GET https://connect.mindcloud.co/v1/universal/merrenIO/latest/actions/view-individual-table-and-pie-chart-responses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MerrenIO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/merrenIO/latest/actions/view-individual-table-and-pie-chart-responses?connectionId=$CONNECTION_ID&surveyId=680000000000000000000000" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "surveyId": "680000000000000000000000"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/merrenIO/latest/actions/view-individual-table-and-pie-chart-responses?${params}`, {
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
| `surveyId` | string | yes | Survey identifier to summarize. Example: `680000000000000000000000`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MerrenIO API returns.

## Native endpoint

Through the native MerrenIO API, this operation is `GET /survey/getQuestionSummary/:surveyId` (base URL `https://app.merren.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/view-individual-table-and-pie-chart-responses.md) for the provider-specific parameters and requirements.

