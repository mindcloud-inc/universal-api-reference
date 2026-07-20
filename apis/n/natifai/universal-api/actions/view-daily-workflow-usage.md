# Natif.ai: View Daily Workflow Usage

Retrieves daily usage details for a Natif.ai workflow.

```
GET https://connect.mindcloud.co/v1/universal/natifai/latest/actions/view-daily-workflow-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Natif.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/natifai/latest/actions/view-daily-workflow-usage?connectionId=$CONNECTION_ID&workflowId=string&start=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workflowId": "string",
  "start": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/natifai/latest/actions/view-daily-workflow-usage?${params}`, {
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
| `workflowId` | string | yes | Workflow identifier. |
| `start` | string | yes | Start date in `%Y-%m-%d` format. |
| `end` | string | no | Optional end date in `%Y-%m-%d` format. Span must be at most 30 days. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `extended` | boolean | no | Include documents, pages, and average processing time per page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "average_time_per_page": 1,
      "date": "string",
      "num_documents": 1,
      "num_pages": 1,
      "processed_credits": 1,
      "which": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `average_time_per_page` | number |  |
| `date` | string |  |
| `num_documents` | number |  |
| `num_pages` | number |  |
| `processed_credits` | number |  |
| `which` | string |  |

## Native endpoint

Through the native Natif.ai API, this operation is `GET /processing/[:workflowId]/usage/daily` (base URL `https://api.natif.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/view-daily-workflow-usage.md) for the provider-specific parameters and requirements.

