# Microsoft Dynamics 365 BC: Update Ship-to Addresses SSI



```
PUT https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/update-ship-to-addresses-ssi
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Dynamics 365 BC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/update-ship-to-addresses-ssi" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/update-ship-to-addresses-ssi', {
  method: 'PUT',
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
| `company_id` | string | no |  |
| `code` | string | no |  |
| `customerNo` | string | no |  |
| `shipToAddressCode` | string | no |  |
| `address` | string | no |  |
| `address2` | string | no |  |
| `city` | string | no |  |
| `contact` | string | no |  |
| `countryRegionCode` | string | no |  |
| `county` | string | no |  |
| `email` | string | no |  |
| `faxNo` | string | no |  |
| `gln` | string | no |  |
| `lastDateModified` | string | no |  |
| `locationCode` | string | no |  |
| `name` | string | no |  |
| `name2` | string | no |  |
| `phoneNo` | string | no |  |
| `postCode` | string | no |  |
| `salespersonCode` | string | no |  |
| `satAddressId` | string | no |  |
| `shipmentMethodCode` | string | no |  |
| `shippingAgentCode` | string | no |  |
| `shippingAgentServiceCode` | string | no |  |
| `taxAreaCode` | string | no |  |
| `taxLiable` | string | no |  |
| `upsZone` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Dynamics 365 BC API returns.

## Native endpoint

Through the native Microsoft Dynamics 365 BC API, this operation is `PATCH v2.0/companies(:company_id)/shipToAddressesSSI(CustomerNo=':customerNo',Code=':shipToAddressCode')` (base URL `https://api.businesscentral.dynamics.com/v2.0/{{credentials.tenantId}}/{{credentials.environment}}/api/ssi/aapi/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-ship-to-addresses-ssi.md) for the provider-specific parameters and requirements.

