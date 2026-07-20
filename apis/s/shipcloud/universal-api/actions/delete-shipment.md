# Shipcloud: Delete Shipment

Deletes an existing shipment from Shipcloud.

```
DELETE https://connect.mindcloud.co/v1/universal/shipcloud/latest/actions/delete-shipment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shipcloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/shipcloud/latest/actions/delete-shipment?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shipcloud/latest/actions/delete-shipment?${params}`, {
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
| `id` | string | yes | The Shipcloud shipment identifier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Shipcloud API returns.

## Native endpoint

Through the native Shipcloud API, this operation is `DELETE /shipments/:id` (base URL `https://api.shipcloud.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-shipment.md) for the provider-specific parameters and requirements.

