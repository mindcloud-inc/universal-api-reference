# Viewpoint Vista: Upsert Invoice Batch

Upsert Invoice Batch

```
POST https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/upsert-invoice-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewpoint Vista `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/upsert-invoice-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "co": 1,
  "mth": "2026-05-01"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/upsert-invoice-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "co": 1,
    "mth": "2026-05-01"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `co` | number | yes | Vista PR company. |
| `mth` | string | yes | Posting month for the batch. Format: YYYY-MM-DD. Example: `2026-05-01`. |
| `notes` | string | no | Optional notes for the timecard batch. |
| `__batch` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "operation": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `operation` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Viewpoint Vista API, this operation is `POST v1/direct/subscribers/{{credentials.subscriberCode}}/vista/pr/2/data/batches/actions/upsert_invoice` (base URL `https://api.xchange.trimble.com/connect/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-invoice-batch.md) for the provider-specific parameters and requirements.

