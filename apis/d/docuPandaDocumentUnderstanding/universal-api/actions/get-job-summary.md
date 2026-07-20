# DocuPanda - Document Understanding: Get Job Count

Retrieves job counts from DocuPanda.

```
GET https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/get-job-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPanda - Document Understanding `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/get-job-summary?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/get-job-summary?${params}`, {
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
| `include_daily_usage` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dailyUsage": [
        {}
      ],
      "summaryAllTime": {},
      "summaryRecent": {},
      "totalVisibleJobs": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dailyUsage` | array<object> | Daily credit usage broken down by job type. |
| `summaryAllTime` | object | Summary of the total number of jobs and credits used by job type (deleted jobs count as well). |
| `summaryRecent` | object | Summary of the recent (since last billing cycle) number of jobs and credits used by job type. |
| `totalVisibleJobs` | number | Total number of visible jobs (not deleted). |

## Native endpoint

Through the native DocuPanda - Document Understanding API, this operation is `GET /jobs/summary` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job-summary.md) for the provider-specific parameters and requirements.

