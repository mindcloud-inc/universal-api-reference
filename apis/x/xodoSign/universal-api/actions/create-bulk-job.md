# Xodo Sign: Create Bulk Job

Creates a new bulk job in Xodo Sign.

```
POST https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/create-bulk-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xodo Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/create-bulk-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "business_id": "string",
  "templateHash": "string",
  "rows[]": [
    [
      "string"
    ]
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/create-bulk-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "business_id": "string",
    "templateHash": "string",
    "rows[]": [["string"]]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `business_id` | string | yes | Business ID to scope the bulk job request. |
| `templateHash` | string | yes | Template hash used for the bulk sending job. |
| `rows[]` | array<array> | yes | Two-dimensional array payload for the bulk job. The first row is the header row and each following row is one bulk-send record. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "business_id": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "document_count": 1,
      "entry_id": 1,
      "status": "string",
      "template_hash": "string",
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `business_id` | number | Business ID that created the bulk job. |
| `created_at` | date | Creation timestamp of the bulk job in UTC. |
| `document_count` | number | Number of documents created by the job. |
| `entry_id` | number | Unique database ID of the bulk job. |
| `status` | string | Current bulk job status returned by Xodo Sign. |
| `template_hash` | string | Template hash used for the job. |
| `user_id` | number | User ID that requested the job. |

## Native endpoint

Through the native Xodo Sign API, this operation is `POST /template/:templateHash/bulk/job` (base URL `https://api.eversign.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-bulk-job.md) for the provider-specific parameters and requirements.

