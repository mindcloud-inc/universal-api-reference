# Viewpoint Vista: Cancel Change Order Batch



```
DELETE https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/cancel-change-order-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewpoint Vista `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/cancel-change-order-batch?connectionId=$CONNECTION_ID&co=1&mth=2026-05-01&batchId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "co": "1",
  "mth": "2026-05-01",
  "batchId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/cancel-change-order-batch?${params}`, {
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
| `co` | number | yes | Vista company for the change order batch. Allowed range: 1 to 255. |
| `mth` | string | yes | Posting month for the batch. Format: YYYY-MM-01. Example: `2026-05-01`. |
| `batchId` | number | yes | Change order batch ID to cancel. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clearBatch` | boolean | no | When true, clears entries in the batch before cancellation. Omit or set false to fail when entries remain. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Viewpoint Vista API returns.

## Native endpoint

Through the native Viewpoint Vista API, this operation is `POST v1/direct/subscribers/{{credentials.subscriberCode}}/vista/po/2/data/co_batches/actions/cancel` (base URL `https://api.xchange.trimble.com/connect/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-change-order-batch.md) for the provider-specific parameters and requirements.

