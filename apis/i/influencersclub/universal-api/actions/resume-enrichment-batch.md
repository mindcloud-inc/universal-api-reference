# Influencers.club: Resume Enrichment Batch

Resumes a paused batch enrichment job in Influencers.club.

```
PUT https://connect.mindcloud.co/v1/universal/influencersclub/latest/actions/resume-enrichment-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Influencers.club `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/influencersclub/latest/actions/resume-enrichment-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "batchId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/influencersclub/latest/actions/resume-enrichment-batch', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "batchId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `batchId` | string | yes | Batch identifier to resume processing. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Influencers.club API returns.

## Native endpoint

Through the native Influencers.club API, this operation is `POST /public/v1/enrichment/batch/:batch_id/resume/` (base URL `https://api-dashboard.influencers.club`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/resume-enrichment-batch.md) for the provider-specific parameters and requirements.

