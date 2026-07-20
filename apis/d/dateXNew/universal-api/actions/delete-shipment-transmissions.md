# DateX: Delete Shipment Transmissions



```
DELETE https://connect.mindcloud.co/v1/universal/dateXNew/latest/actions/delete-shipment-transmissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DateX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/dateXNew/latest/actions/delete-shipment-transmissions?connectionId=$CONNECTION_ID&shipmentIds%5B%5D=12345" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "shipmentIds[]": "12345"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dateXNew/latest/actions/delete-shipment-transmissions?${params}`, {
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
| `shipmentIds[]` | array<number> | yes | Shipment IDs whose transmissions should be deleted. Example: `12345`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "shipmentId": 1,
      "succeeded": true,
      "transmissionsDeleted": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `shipmentId` | number |  |
| `succeeded` | boolean |  |
| `transmissionsDeleted` | number |  |

## Native endpoint

Through the native DateX API, this operation is `POST sales_orders/shipments/transmissions/delete` (base URL `https://{{credentials.environment}}.wavelength.host/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-shipment-transmissions.md) for the provider-specific parameters and requirements.

