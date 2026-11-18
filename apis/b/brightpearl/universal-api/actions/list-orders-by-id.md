# Brightpearl: List Orders by ID



```
GET https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/list-orders-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brightpearl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/list-orders-by-id?connectionId=$CONNECTION_ID&orderIds=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderIds": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/list-orders-by-id?${params}`, {
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
| `orderIds` | string | yes | One order ID, comma-separated IDs, or ID ranges such as 100-120,130. Request at most 200 orders per call; use Order OPTIONS for larger sets. |
| `includeOptional` | list<string> | no | Optional comma-separated sections: customFields,nullCustomFields. One of: `customFields`, `nullCustomFields`. Accepts multiple values in one string, delimited by `,`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acknowledged": 1,
      "allocationStatusCode": "string",
      "assignment": {
        "current": {
          "channelId": 1,
          "channeltId": 1,
          "leadSourceId": 1,
          "projectId": 1,
          "staffOwnerContactId": 1,
          "teamId": 1
        }
      },
      "closedOn": "2026-05-07T12:00:00.000Z",
      "costPriceListId": 1,
      "createdById": 1,
      "createdOn": "2026-05-07T12:00:00.000Z",
      "currency": {
        "accountingCurrencyCode": "string",
        "exchangeRate": "string",
        "fixedExchangeRate": true,
        "orderCurrencyCode": "string"
      },
      "customFields": {
        "PCF_COLOR": {
          "id": 1,
          "value": "string"
        },
        "PCF_FRETS": 1,
        "PCF_SCALE": 1
      },
      "delivery": {
        "deliveryDate": "2026-05-07T12:00:00.000Z",
        "shippingMethodId": 1
      },
      "historicalOrder": true,
      "id": 1,
      "invoices": [
        {
          "dueDate": "2026-05-07T12:00:00.000Z",
          "invoiceReference": "string",
          "taxDate": "2026-05-07T12:00:00.000Z"
        }
      ],
      "isDropship": true,
      "nullCustomFields": [
        "string"
      ],
      "orderPaymentStatus": "string",
      "orderRows": {},
      "orderStatus": {
        "name": "Ava Chen",
        "orderStatusId": 1
      },
      "orderTypeCode": "string",
      "parentOrderId": 1,
      "parties": {
        "billing": {
          "addressFullName": "Ava Chen",
          "addressLine1": "string",
          "addressLine2": "string",
          "addressLine3": "string",
          "addressLine4": "string",
          "companyName": "Ava Chen",
          "contactId": 1,
          "country": "string",
          "countryId": 1,
          "countryIsoCode": "string",
          "countryIsoCode3": "string",
          "email": "ava@example.com",
          "mobileTelephone": "string",
          "postalCode": "string",
          "telephone": "string"
        },
        "customer": {
          "addressFullName": "Ava Chen",
          "addressLine1": "string",
          "addressLine2": "string",
          "addressLine3": "string",
          "addressLine4": "string",
          "companyName": "Ava Chen",
          "contactId": 1,
          "country": "string",
          "countryId": 1,
          "countryIsoCode": "string",
          "countryIsoCode3": "string",
          "email": "ava@example.com",
          "mobileTelephone": "string",
          "postalCode": "string",
          "telephone": "string"
        },
        "delivery": {
          "addressFullName": "Ava Chen",
          "addressLine1": "string",
          "addressLine2": "string",
          "addressLine3": "string",
          "addressLine4": "string",
          "companyName": "Ava Chen",
          "country": "string",
          "countryId": 1,
          "countryIsoCode": "string",
          "countryIsoCode3": "string",
          "email": "ava@example.com",
          "mobileTelephone": "string",
          "postalCode": "string",
          "telephone": "string"
        },
        "supplier": {
          "addressFullName": "Ava Chen",
          "addressLine1": "string",
          "addressLine2": "string",
          "addressLine3": "string",
          "addressLine4": "string",
          "companyName": "Ava Chen",
          "contactId": 1,
          "country": "string",
          "countryIsoCode": "string",
          "countryIsoCode3": "string",
          "email": "ava@example.com",
          "mobileTelephone": "string",
          "postalCode": "string",
          "telephone": "string"
        }
      },
      "placedOn": "2026-05-07T12:00:00.000Z",
      "priceListId": 1,
      "priceModeCode": "string",
      "reference": "string",
      "shippingStatusCode": "string",
      "state": {
        "tax": "string"
      },
      "stockStatusCode": "string",
      "tax": {
        "errors": [
          "string"
        ]
      },
      "totalValue": {
        "baseNet": "string",
        "baseTaxAmount": "string",
        "baseTotal": "string",
        "net": "string",
        "taxAmount": "string",
        "total": "string"
      },
      "updatedOn": "2026-05-07T12:00:00.000Z",
      "version": 1,
      "warehouseId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acknowledged` | number |  |
| `allocationStatusCode` | string |  |
| `assignment` | object |  |
| `assignment.current` | object |  |
| `assignment.current.channelId` | number |  |
| `assignment.current.channeltId` | number |  |
| `assignment.current.leadSourceId` | number |  |
| `assignment.current.projectId` | number |  |
| `assignment.current.staffOwnerContactId` | number |  |
| `assignment.current.teamId` | number |  |
| `closedOn` | date |  |
| `costPriceListId` | number |  |
| `createdById` | number |  |
| `createdOn` | date |  |
| `currency` | object |  |
| `currency.accountingCurrencyCode` | string |  |
| `currency.exchangeRate` | string |  |
| `currency.fixedExchangeRate` | boolean |  |
| `currency.orderCurrencyCode` | string |  |
| `customFields` | object |  |
| `customFields.PCF_COLOR` | object |  |
| `customFields.PCF_COLOR.id` | number |  |
| `customFields.PCF_COLOR.value` | string |  |
| `customFields.PCF_FRETS` | number |  |
| `customFields.PCF_SCALE` | number |  |
| `delivery` | object |  |
| `delivery.deliveryDate` | date |  |
| `delivery.shippingMethodId` | number |  |
| `historicalOrder` | boolean |  |
| `id` | number |  |
| `invoices` | array<object> |  |
| `invoices[].dueDate` | date |  |
| `invoices[].invoiceReference` | string |  |
| `invoices[].taxDate` | date |  |
| `isDropship` | boolean |  |
| `nullCustomFields` | array<string> |  |
| `orderPaymentStatus` | string |  |
| `orderRows` | object |  |
| `orderStatus` | object |  |
| `orderStatus.name` | string |  |
| `orderStatus.orderStatusId` | number |  |
| `orderTypeCode` | string |  |
| `parentOrderId` | number |  |
| `parties` | object |  |
| `parties.billing` | object |  |
| `parties.billing.addressFullName` | string |  |
| `parties.billing.addressLine1` | string |  |
| `parties.billing.addressLine2` | string |  |
| `parties.billing.addressLine3` | string |  |
| `parties.billing.addressLine4` | string |  |
| `parties.billing.companyName` | string |  |
| `parties.billing.contactId` | number |  |
| `parties.billing.country` | string |  |
| `parties.billing.countryId` | number |  |
| `parties.billing.countryIsoCode` | string |  |
| `parties.billing.countryIsoCode3` | string |  |
| `parties.billing.email` | string |  |
| `parties.billing.mobileTelephone` | string |  |
| `parties.billing.postalCode` | string |  |
| `parties.billing.telephone` | string |  |
| `parties.customer` | object |  |
| `parties.customer.addressFullName` | string |  |
| `parties.customer.addressLine1` | string |  |
| `parties.customer.addressLine2` | string |  |
| `parties.customer.addressLine3` | string |  |
| `parties.customer.addressLine4` | string |  |
| `parties.customer.companyName` | string |  |
| `parties.customer.contactId` | number |  |
| `parties.customer.country` | string |  |
| `parties.customer.countryId` | number |  |
| `parties.customer.countryIsoCode` | string |  |
| `parties.customer.countryIsoCode3` | string |  |
| `parties.customer.email` | string |  |
| `parties.customer.mobileTelephone` | string |  |
| `parties.customer.postalCode` | string |  |
| `parties.customer.telephone` | string |  |
| `parties.delivery` | object |  |
| `parties.delivery.addressFullName` | string |  |
| `parties.delivery.addressLine1` | string |  |
| `parties.delivery.addressLine2` | string |  |
| `parties.delivery.addressLine3` | string |  |
| `parties.delivery.addressLine4` | string |  |
| `parties.delivery.companyName` | string |  |
| `parties.delivery.country` | string |  |
| `parties.delivery.countryId` | number |  |
| `parties.delivery.countryIsoCode` | string |  |
| `parties.delivery.countryIsoCode3` | string |  |
| `parties.delivery.email` | string |  |
| `parties.delivery.mobileTelephone` | string |  |
| `parties.delivery.postalCode` | string |  |
| `parties.delivery.telephone` | string |  |
| `parties.supplier` | object |  |
| `parties.supplier.addressFullName` | string |  |
| `parties.supplier.addressLine1` | string |  |
| `parties.supplier.addressLine2` | string |  |
| `parties.supplier.addressLine3` | string |  |
| `parties.supplier.addressLine4` | string |  |
| `parties.supplier.companyName` | string |  |
| `parties.supplier.contactId` | number |  |
| `parties.supplier.country` | string |  |
| `parties.supplier.countryIsoCode` | string |  |
| `parties.supplier.countryIsoCode3` | string |  |
| `parties.supplier.email` | string |  |
| `parties.supplier.mobileTelephone` | string |  |
| `parties.supplier.postalCode` | string |  |
| `parties.supplier.telephone` | string |  |
| `placedOn` | date |  |
| `priceListId` | number |  |
| `priceModeCode` | string |  |
| `reference` | string |  |
| `shippingStatusCode` | string |  |
| `state` | object |  |
| `state.tax` | string |  |
| `stockStatusCode` | string |  |
| `tax` | object |  |
| `tax.errors` | array |  |
| `totalValue` | object |  |
| `totalValue.baseNet` | string |  |
| `totalValue.baseTaxAmount` | string |  |
| `totalValue.baseTotal` | string |  |
| `totalValue.net` | string |  |
| `totalValue.taxAmount` | string |  |
| `totalValue.total` | string |  |
| `updatedOn` | date |  |
| `version` | number |  |
| `warehouseId` | number |  |

## Native endpoint

Through the native Brightpearl API, this operation is `GET /order-service/order/:orderIds` (base URL `https://{{credentials.apiDomain}}/public-api/{{credentials.account}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-orders-by-id.md) for the provider-specific parameters and requirements.

