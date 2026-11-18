# Brightpearl: Create Order



```
POST https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/create-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brightpearl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderTypeCode": "PC"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/create-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderTypeCode": "PC"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderTypeCode` | list<string> | yes | One of: `PC`, `PO`, `SC`, `SO`. |
| `parties` | object | no |  |
| `parties.customer` | object | no |  |
| `parties.customer.contactId` | number | no | Required for sales orders (SO) and sales credits (SC). |
| `parties.supplier` | object | no |  |
| `parties.supplier.contactId` | number | no | Required for purchase orders (PO) and purchase credits (PC). |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `reference` | string | no |  |
| `parentOrderId` | string | no |  |
| `priceListId` | number | no |  |
| `costPriceListId` | number | no |  |
| `priceModeCode` | list<string> | no | Applies to sales orders and sales credits. One of: `EXC`, `INC`. |
| `placedOn` | date | no |  |
| `orderStatus` | object | no |  |
| `orderStatus.orderStatusId` | number | no |  |
| `delivery` | object | no |  |
| `delivery.deliveryDate` | date | no |  |
| `delivery.shippingMethodId` | number | no |  |
| `invoices[]` | array<object> | no |  |
| `invoices[].taxDate` | date | no |  |
| `currency` | object | no |  |
| `currency.orderCurrencyCode` | string | no |  |
| `currency.fixedExchangeRate` | boolean | no |  |
| `currency.exchangeRate` | string | no | Up to six decimal places. Requires fixed exchange rate. |
| `parties.delivery` | object | no |  |
| `parties.delivery.addressFullName` | string | no |  |
| `parties.delivery.companyName` | string | no |  |
| `parties.delivery.addressLine1` | string | no |  |
| `parties.delivery.addressLine2` | string | no |  |
| `parties.delivery.addressLine3` | string | no |  |
| `parties.delivery.addressLine4` | string | no |  |
| `parties.delivery.postalCode` | string | no |  |
| `parties.delivery.countryId` | string | no | When providing a delivery address, supply country ID or country ISO code. |
| `parties.delivery.countryIsoCode` | string | no | When providing a delivery address, supply country ID or country ISO code. |
| `parties.delivery.telephone` | string | no |  |
| `parties.delivery.mobileTelephone` | string | no |  |
| `parties.delivery.fax` | string | no |  |
| `parties.delivery.email` | string | no |  |
| `assignment` | object | no |  |
| `assignment.current` | object | no |  |
| `assignment.current.channelId` | number | no |  |
| `assignment.current.leadSourceId` | number | no |  |
| `assignment.current.projectId` | number | no |  |
| `assignment.current.staffOwnerContactId` | number | no |  |
| `assignment.current.teamId` | number | no |  |
| `warehouseId` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |

## Native endpoint

Through the native Brightpearl API, this operation is `POST /order-service/order/` (base URL `https://{{credentials.apiDomain}}/public-api/{{credentials.account}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order.md) for the provider-specific parameters and requirements.

