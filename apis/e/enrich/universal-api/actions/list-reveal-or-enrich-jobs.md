# Enrich.so: List Reveal Or Enrich Jobs

Retrieves reveal or enrich jobs from Enrich.so.

```
GET https://connect.mindcloud.co/v1/universal/enrich/latest/actions/list-reveal-or-enrich-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Enrich.so `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/enrich/latest/actions/list-reveal-or-enrich-jobs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/enrich/latest/actions/list-reveal-or-enrich-jobs?${params}`, {
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
| `status` | string | no | Optional job status filter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "jobId": "string",
      "processedItems": 1,
      "status": "string",
      "totalItems": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completedAt` | date | Job completion timestamp. |
| `createdAt` | date | Job creation timestamp. |
| `jobId` | string | Reveal or enrich job identifier. |
| `processedItems` | number | Items processed so far. |
| `status` | string | Current job status. |
| `totalItems` | number | Total items in the job. |
| `type` | string | Reveal or enrich job type. |

## Native endpoint

Through the native Enrich.so API, this operation is `GET /lead-finder/reveal-jobs` (base URL `https://dev.enrich.so/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-reveal-or-enrich-jobs.md) for the provider-specific parameters and requirements.

