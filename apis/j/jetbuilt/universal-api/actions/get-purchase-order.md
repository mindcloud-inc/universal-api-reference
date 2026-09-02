# Jetbuilt: Get Purchase Order



```
GET https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/get-purchase-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jetbuilt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/get-purchase-order?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/get-purchase-order?${params}`, {
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
| `id` | string | yes |  |
| `project_id` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customId": "string",
      "defaultShip": "string",
      "id": 1,
      "notes": "string",
      "projectId": 1,
      "purchasingSourceId": 1,
      "shipAddress": {
        "city": "Ava Chen",
        "country": "string",
        "postalCode": "string",
        "region": "string",
        "street": "string"
      },
      "shipName": "Ava Chen",
      "shippingOption": "string",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `customId` | string |  |
| `defaultShip` | string |  |
| `id` | number |  |
| `notes` | string |  |
| `projectId` | number |  |
| `purchasingSourceId` | number |  |
| `shipAddress.city` | string |  |
| `shipAddress.country` | string |  |
| `shipAddress.postalCode` | string |  |
| `shipAddress.region` | string |  |
| `shipAddress.street` | string |  |
| `shipName` | string |  |
| `shippingOption` | string |  |
| `status` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Jetbuilt API, this operation is `GET purchase_orders/[:id]` (base URL `https://app.jetbuilt.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-purchase-order.md) for the provider-specific parameters and requirements.

