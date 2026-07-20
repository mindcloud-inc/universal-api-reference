# Microsoft Dynamics 365 BC: Update Sales Order SSI



```
POST https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/update-sales-order-ssi
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Dynamics 365 BC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/update-sales-order-ssi" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/update-sales-order-ssi', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | no |  |
| `salesOrderID` | string | no |  |
| `salesforceOrderNo` | string | no |  |
| `shipToCode` | string | no |  |
| `billAndHoldReturnSSI` | boolean | no |  |
| `billToAddress2` | string | no |  |
| `billToContactNo` | string | no |  |
| `billToCountryRegionCode` | string | no |  |
| `billToCounty` | string | no |  |
| `billToCustomerNo` | string | no |  |
| `billToName` | string | no |  |
| `billToPostCode` | string | no |  |
| `currencyCode` | string | no |  |
| `currencyCode` | string | no |  |
| `customerDiscCode` | string | no |  |
| `customerPriceGroup` | string | no |  |
| `documentDate` | string | no |  |
| `documentType` | string | no |  |
| `dropShipVendorNoSSI` | string | no |  |
| `dueDate` | string | no |  |
| `dueDate` | string | no |  |
| `earliestShipDateSSI` | string | no |  |
| `earliestShipDateSSI` | string | no |  |
| `externalDocumentNo` | string | no |  |
| `externalDocumentNo` | string | no |  |
| `invoiceDiscCode` | string | no |  |
| `itemsShipBeforeInvoiceSSI` | boolean | no |  |
| `itemsShipBeforeInvoiceSSI` | boolean | no |  |
| `latestShipDateSSI` | string | no |  |
| `latestShipDateSSI` | string | no |  |
| `locationCode` | string | no |  |
| `no` | string | no |  |
| `orderDate` | string | no |  |
| `orderStatusSSI` | string | no |  |
| `orderStatusSSI` | string | no |  |
| `orderTypeSSI` | string | no |  |
| `paymentDiscountPercent` | number | no |  |
| `paymentMethodCode` | string | no |  |
| `paymentTermsCode` | string | no |  |
| `pmtDiscountDate` | string | no |  |
| `postingDate` | string | no |  |
| `pricesIncludingVAT` | boolean | no |  |
| `prmisedDeliveryDate` | string | no |  |
| `requestedDeliveryDate` | string | no |  |
| `requestedDeliveryDate` | string | no |  |
| `salespersonCode` | string | no |  |
| `salespersonCode` | string | no |  |
| `sellToAddress` | string | no |  |
| `sellToAddress2` | string | no |  |
| `sellToCity` | string | no |  |
| `sellToContact` | string | no |  |
| `sellToContactNo` | string | no |  |
| `sellToCountryRegionCode` | string | no |  |
| `sellToCounty` | string | no |  |
| `sellToCustomerName` | string | no |  |
| `sellToCustomerName2` | string | no |  |
| `sellToCustomerNo` | string | no |  |
| `sellToEmail` | string | no |  |
| `sellToPhoneNo` | string | no |  |
| `sellToPostCode` | string | no |  |
| `shipmentDate` | string | no |  |
| `shipmentMethodCode` | string | no |  |
| `shippingAgentCode` | string | no |  |
| `shippingAgentServiceCode` | string | no |  |
| `shippingInstructionsSSI` | string | no |  |
| `shippingInstructionsSSI` | string | no |  |
| `shipToAddress` | string | no |  |
| `shipToContact` | string | no |  |
| `shipToCountryRegionCode` | string | no |  |
| `shipToCounty` | string | no |  |
| `shipToName` | string | no |  |
| `shipToPhoneNo` | string | no |  |
| `shipToPhoneNo` | string | no |  |
| `shipToPostCode` | string | no |  |
| `shortcutDimension1Code` | string | no |  |
| `shortcutDimension2Code` | string | no |  |
| `taxAreaCode` | string | no |  |
| `taxAreaCode` | string | no |  |
| `taxLiable` | boolean | no |  |
| `taxLiable` | boolean | no |  |
| `vatCountryRegionCode` | string | no |  |
| `vatRegistrationNo` | string | no |  |
| `vatRegistrationNo` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Dynamics 365 BC API returns.

## Native endpoint

Through the native Microsoft Dynamics 365 BC API, this operation is `PATCH /v2.0/companies(:id)/salesHeadersSSI(:salesOrderID)` (base URL `https://api.businesscentral.dynamics.com/v2.0/{{credentials.tenantId}}/{{credentials.environment}}/api/ssi/aapi/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-sales-order-ssi.md) for the provider-specific parameters and requirements.

