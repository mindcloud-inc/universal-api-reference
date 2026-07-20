# 100Hires ATS: List Applications

Lists the applications in 100Hires ATS.

```
GET https://connect.mindcloud.co/v1/universal/hiresATS/latest/actions/list-applications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 100Hires ATS `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hiresATS/latest/actions/list-applications?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hiresATS/latest/actions/list-applications?${params}`, {
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
| `candidateId` | number | no | Return only applications for this candidate ID. Example: `4694640`. |
| `jobId` | number | no | Return only applications for this job ID. Example: `275691`. |
| `stageId` | number | no | Return only applications in this stage ID. Example: `251850`. |
| `status` | string | no | Filter by application status: pending, hired, or rejected. Example: `pending`. |
| `createdAfter` | date | no | Return only applications created after this Unix timestamp. Example: `1774543600`. |
| `updatedAfter` | date | no | Return only applications updated after this Unix timestamp. Example: `1774543600`. |
| `aiScoreMin` | number | no | Return only applications with AI score at or above this value. Example: `75`. |
| `aiScoreMax` | number | no | Return only applications with AI score at or below this value. Example: `95`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sort` | string | no | Sort order: created_at, -created_at, ai_score, or -ai_score. Example: `-created_at`. |
| `include` | string | no | Comma-separated related application resources to include. Example: `candidate,job`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 100Hires ATS API returns.

## Native endpoint

Through the native 100Hires ATS API, this operation is `GET /applications` (base URL `https://api.100hires.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-applications.md) for the provider-specific parameters and requirements.

