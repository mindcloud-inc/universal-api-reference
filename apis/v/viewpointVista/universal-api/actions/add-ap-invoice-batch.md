# Viewpoint Vista: Add AP Invoice Batch



```
POST https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/add-ap-invoice-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewpoint Vista `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/add-ap-invoice-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "co": 1,
  "mth": "2026-09-01"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/add-ap-invoice-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "co": 1,
    "mth": "2026-09-01"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `co` | number | yes | AP company. Allowed range: 1 to 255. |
| `mth` | string | yes | Posting month for the invoice batch. Format: YYYY-MM-01. Example: `2026-09-01`. |
| `notes` | string | no | Optional notes for the invoice batch. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Viewpoint Vista API returns.

## Native endpoint

Through the native Viewpoint Vista API, this operation is `POST v1/direct/subscribers/{{credentials.subscriberCode}}/vista/ap/2/data/inv_batches/actions/add` (base URL `https://api.xchange.trimble.com/connect/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-ap-invoice-batch.md) for the provider-specific parameters and requirements.

