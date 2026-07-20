# Parallel Web Systems: Create FindAll Run



```
POST https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/create-find-all-run
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Parallel Web Systems `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/create-find-all-run" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/create-find-all-run', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "findall_id": "string",
      "generator": "string",
      "modified_at": "2026-05-07T12:00:00.000Z",
      "status": {
        "is_active": true,
        "metrics": {
          "generated_candidates_count": 1,
          "matched_candidates_count": 1
        },
        "status": "string",
        "termination_reason": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | FindAll run creation timestamp. |
| `findall_id` | string | FindAll run identifier. |
| `generator` | string | Candidate generator. |
| `modified_at` | date | Last FindAll run update timestamp. |
| `status.is_active` | boolean | Whether the FindAll run is active. |
| `status.metrics.generated_candidates_count` | number | Generated candidate count. |
| `status.metrics.matched_candidates_count` | number | Matched candidate count. |
| `status.status` | string | FindAll run status. |
| `status.termination_reason` | string | Termination reason when present. |

## Native endpoint

Through the native Parallel Web Systems API, this operation is `POST /v1beta/findall/runs` (base URL `https://api.parallel.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-find-all-run.md) for the provider-specific parameters and requirements.

