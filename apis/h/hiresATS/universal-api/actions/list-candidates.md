# 100Hires ATS: List Candidates

Lists the candidates in 100Hires ATS.

```
GET https://connect.mindcloud.co/v1/universal/hiresATS/latest/actions/list-candidates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 100Hires ATS `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hiresATS/latest/actions/list-candidates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hiresATS/latest/actions/list-candidates?${params}`, {
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
| `search` | string | no | Optional search by candidate name or email. |
| `email` | string | no | Optional exact email filter. |
| `fullName` | string | no | Optional full-name filter. |
| `jobId` | number | no | Optional job ID to filter candidates by job. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `linkedin` | string | no | Optional LinkedIn URL or alias filter. |
| `companyId` | number | no | Optional target company ID. Defaults to the authenticated company. |
| `createdAfter` | number | no | Optional Unix timestamp (seconds) lower bound for created_at. |
| `updatedAfter` | number | no | Optional Unix timestamp (seconds) lower bound for updated_at. |
| `include` | string | no | Optional include selector for related application summaries. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 100Hires ATS API returns.

## Native endpoint

Through the native 100Hires ATS API, this operation is `GET /candidates` (base URL `https://api.100hires.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-candidates.md) for the provider-specific parameters and requirements.

