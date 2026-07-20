# Influencers.club: Create Enrichment Batch

Creates a batch enrichment job in Influencers.club from a CSV.

```
POST https://connect.mindcloud.co/v1/universal/influencersclub/latest/actions/create-enrichment-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Influencers.club `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/influencersclub/latest/actions/create-enrichment-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string",
  "enrichmentMode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/influencersclub/latest/actions/create-enrichment-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string",
    "enrichmentMode": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | string | yes | CSV file (single column handle or email). |
| `enrichmentMode` | string | yes | Mode: raw, full, basic, or advanced. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `platform` | string | no | Platform for handle-based enrichment batches. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "batch_id": "string",
      "created_at": "string",
      "enrichment_mode": "string",
      "message": "string",
      "metadata": {},
      "og_input_number": 1,
      "platform": "string",
      "status": "string",
      "type_report": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `batch_id` | string | Created batch identifier. |
| `created_at` | string | Batch creation timestamp. |
| `enrichment_mode` | string | Selected enrichment mode. |
| `message` | string | Human-readable status message. |
| `metadata` | object | Additional metadata for the batch. |
| `og_input_number` | number | Total number of rows in input file. |
| `platform` | string | Target platform. |
| `status` | string | Current batch status. |
| `type_report` | string | Report type (for example ENRICH_BY_HANDLE or ENRICH_BY_EMAIL). |

## Native endpoint

Through the native Influencers.club API, this operation is `POST /public/v1/enrichment/batch/` (base URL `https://api-dashboard.influencers.club`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-enrichment-batch.md) for the provider-specific parameters and requirements.

