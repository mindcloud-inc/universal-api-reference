# PagePixels: List All Website Domain Research Reports



```
GET https://connect.mindcloud.co/v1/universal/pagePixels/latest/actions/list-all-website-domain-research-reports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PagePixels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pagePixels/latest/actions/list-all-website-domain-research-reports?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pagePixels/latest/actions/list-all-website-domain-research-reports?${params}`, {
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
| `page` | number | no | The page to retrieve. |
| `limit` | number | no | The maximum number of reports to return. |
| `after` | number | no | Only return reports created after this unix timestamp. |
| `before` | number | no | Only return reports created before this unix timestamp. |
| `order` | string | no | Sort order: ASC or DESC. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedDomains": 1,
      "createdAt": "string",
      "failedDomains": 1,
      "jobId": "string",
      "name": "Ava Chen",
      "status": "string",
      "totalDomains": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completedDomains` | number | The number of domains completed successfully. |
| `createdAt` | string | The creation timestamp for the domain research job. |
| `failedDomains` | number | The number of domains that failed processing. |
| `jobId` | string | The unique identifier for the domain research job. |
| `name` | string | The name of the domain research job. |
| `status` | string | The current provider status for the report job. |
| `totalDomains` | number | The total number of domains included in the job. |

## Native endpoint

Through the native PagePixels API, this operation is `GET /api/domain_research_requests` (base URL `https://api.pagepixels.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-all-website-domain-research-reports.md) for the provider-specific parameters and requirements.

