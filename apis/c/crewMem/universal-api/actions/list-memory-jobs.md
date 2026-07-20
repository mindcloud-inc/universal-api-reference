# CrewMem: List Memory Jobs



```
GET https://connect.mindcloud.co/v1/universal/crewMem/latest/actions/list-memory-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CrewMem `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crewMem/latest/actions/list-memory-jobs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crewMem/latest/actions/list-memory-jobs?${params}`, {
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
| `limit` | number | no | Number of jobs to return |
| `offset` | number | no | Offset for pagination |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "limit": 1,
      "offset": 1,
      "pendingCount": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Provider docs expose a generic data payload; live empty responses currently return null. |
| `limit` | number |  |
| `offset` | number |  |
| `pendingCount` | number | Maps provider pending_count. |
| `success` | boolean |  |

## Native endpoint

Through the native CrewMem API, this operation is `GET /api/memory/jobs` (base URL `https://crewmem.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-memory-jobs.md) for the provider-specific parameters and requirements.

