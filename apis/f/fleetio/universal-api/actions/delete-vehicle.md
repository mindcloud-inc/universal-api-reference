# Fleetio: Delete Vehicle

Deletes an existing vehicle from Fleetio.

```
DELETE https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/delete-vehicle
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fleetio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/delete-vehicle?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/delete-vehicle?${params}`, {
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
| `id` | string | yes | The Fleetio ID of the relevant Vehicle. You may also look up Vehicles by their VIN, license plate, or other external ID. See the guide on [External Vehicle Ids](/docs/guides/vehicles/external-vehicle-ids) for information on how to set this up. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Fleetio API returns.

## Native endpoint

Through the native Fleetio API, this operation is `DELETE vehicles/:id` (base URL `https://secure.fleetio.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-vehicle.md) for the provider-specific parameters and requirements.

