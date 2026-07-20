# Microsoft Dynamics 365 BC: Create Customer SSI



```
POST https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/create-customer-ssi
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Dynamics 365 BC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/create-customer-ssi" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "company_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/create-customer-ssi', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "company_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `address` | string | no |  |
| `company_id` | string | yes |  |
| `county` | string | no |  |
| `paymentMethodCode` | string | no |  |
| `paymentTermsCode` | string | no |  |
| `taxAreaCode` | string | no |  |
| `salesforceCustomerNo` | string | no |  |
| `salespersonCode` | string | no |  |
| `no` | string | no |  |
| `sICCodeSSI` | string | no |  |
| `documentSendingProfile` | string | no |  |
| `name` | string | no |  |
| `genBusPostingGroup` | string | no |  |
| `customerPostingGroup` | string | no |  |
| `addressLine2` | string | no |  |
| `balance` | number | no |  |
| `balanceLCY` | number | no |  |
| `blocked` | string | no |  |
| `city` | string | no |  |
| `contact` | string | no |  |
| `countyRegionCode` | string | no |  |
| `creditLimitLCY` | number | no |  |
| `currencyCode` | string | no |  |
| `currencyId` | string | no |  |
| `email` | string | no |  |
| `gln` | string | no |  |
| `globalDimension1Code` | string | no |  |
| `globalDimension2Code` | string | no |  |
| `invoiceAmounts` | number | no |  |
| `languageCode` | string | no |  |
| `netChange` | number | no |  |
| `netChangeLCY` | number | no |  |
| `phoneNumber` | string | no |  |
| `postCode` | string | no |  |
| `priority` | number | no |  |
| `responsibilityCenter` | string | no |  |
| `salespersonCode` | string | no |  |
| `searchName` | string | no |  |
| `shipmentMethodCode` | string | no |  |
| `shipmentMethodId` | string | no |  |
| `stateInscription` | string | no |  |
| `taxLiable` | boolean | no |  |
| `taxRegistrationNumber` | string | no |  |
| `vatBusPostingGroup` | string | no |  |
| `vatRegistrationNo` | string | no |  |
| `website` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Dynamics 365 BC API returns.

## Native endpoint

Through the native Microsoft Dynamics 365 BC API, this operation is `POST v2.0/companies(:company_id)/customersSSI` (base URL `https://api.businesscentral.dynamics.com/v2.0/{{credentials.tenantId}}/{{credentials.environment}}/api/ssi/aapi/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer-ssi.md) for the provider-specific parameters and requirements.

