# Parallel Web Systems: Retrieve FindAll Run Status



```
GET https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/retrieve-find-all-run-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Parallel Web Systems `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/retrieve-find-all-run-status?connectionId=$CONNECTION_ID&findallId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "findallId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/retrieve-find-all-run-status?${params}`, {
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
| `findallId` | string | yes | The Parallel FindAll run ID. |

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

Through the native Parallel Web Systems API, this operation is `GET /v1beta/findall/runs/:findall_id` (base URL `https://api.parallel.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-find-all-run-status.md) for the provider-specific parameters and requirements.

