# SimpliRoute: Delete Vehicle

Deletes an existing vehicle from SimpliRoute.

```
DELETE https://connect.mindcloud.co/v1/universal/simpliRoute/latest/actions/delete-vehicle
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SimpliRoute `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/simpliRoute/latest/actions/delete-vehicle?connectionId=$CONNECTION_ID&vehicleId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "vehicleId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpliRoute/latest/actions/delete-vehicle?${params}`, {
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
| `vehicleId` | number | yes | The SimpliRoute vehicle ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SimpliRoute API returns.

## Native endpoint

Through the native SimpliRoute API, this operation is `DELETE /v1/routes/vehicles/:vehicle_id/` (base URL `https://api.simpliroute.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-vehicle.md) for the provider-specific parameters and requirements.

