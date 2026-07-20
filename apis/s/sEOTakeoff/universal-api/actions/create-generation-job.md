# SEOTakeoff: Create Generation Job



```
POST https://connect.mindcloud.co/v1/universal/sEOTakeoff/latest/actions/create-generation-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SEOTakeoff `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sEOTakeoff/latest/actions/create-generation-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tenantId": "string",
  "headline": "string",
  "keyword": "string",
  "cluster": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sEOTakeoff/latest/actions/create-generation-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tenantId": "string",
    "headline": "string",
    "keyword": "string",
    "cluster": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tenantId` | string | yes | Tenant slug, like mindcloud-co. |
| `headline` | string | yes | Article headline. |
| `keyword` | string | yes | Target SEO keyword. |
| `cluster` | string | yes | Content cluster name. |
| `headlineId` | string | no | Optional queue item or headline ID for tracking. |
| `language` | string | no | Optional ISO language code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "estimated_time_seconds": 1,
      "job_id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `estimated_time_seconds` | number |  |
| `job_id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native SEOTakeoff API, this operation is `POST /api/v1/generate` (base URL `https://api.seotakeoff.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-generation-job.md) for the provider-specific parameters and requirements.

