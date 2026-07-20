# Restoplace: Update Reservation Status

Updates a reservation status in Restoplace.

```
PUT https://connect.mindcloud.co/v1/universal/restoplace/latest/actions/update-reservation-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Restoplace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/restoplace/latest/actions/update-reservation-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "status": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/restoplace/latest/actions/update-reservation-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "status": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Unique Restoplace reservation ID. |
| `status` | number | yes | Reservation status code. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cancelReason` | number | no | Cancel reason ID from the List Reservation Cancel Reasons action. |
| `cancelReasonText` | string | no | Additional cancel reason text when required by the provider. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Restoplace API returns.

## Native endpoint

Through the native Restoplace API, this operation is `PUT /reserves/:id/status` (base URL `https://api.restoplace.cc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-reservation-status.md) for the provider-specific parameters and requirements.

