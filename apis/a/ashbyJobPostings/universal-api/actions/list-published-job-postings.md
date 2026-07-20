# Ashby Job Postings: List Published Job Postings

Retrieves published job postings from a specific Ashby job board.

```
GET https://connect.mindcloud.co/v1/universal/ashbyJobPostings/latest/actions/list-published-job-postings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ashby Job Postings `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ashbyJobPostings/latest/actions/list-published-job-postings?connectionId=$CONNECTION_ID&job_board_name=Ashby" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "job_board_name": "Ashby"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ashbyJobPostings/latest/actions/list-published-job-postings?${params}`, {
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
| `job_board_name` | string | yes | Required. The final path segment of the Ashby hosted jobs page URL, for example `Ashby` in `https://jobs.ashbyhq.com/Ashby`. Example: `Ashby`. |
| `includeCompensation` | boolean | no | Optional. When true, include compensation data for each returned job posting. Example: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiVersion": "string",
      "jobs": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiVersion` | string | Version identifier returned by the Ashby job postings API. |
| `jobs` | array<object> | Published job postings returned for the requested Ashby job board. |

## Native endpoint

Through the native Ashby Job Postings API, this operation is `GET /posting-api/job-board/:job_board_name` (base URL `https://api.ashbyhq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-published-job-postings.md) for the provider-specific parameters and requirements.

