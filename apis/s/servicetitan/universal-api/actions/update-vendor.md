# ServiceTitan: Update Vendor



```
PUT https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/update-vendor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTitan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/update-vendor" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/update-vendor', {
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
| `address.street` | string | no |  |
| `externalData.applicationGuid` | string | no |  |
| `externalData.externalData[].value` | string | no |  |
| `name` | string | no |  |
| `vendorContacts[].name` | string | no |  |
| `active` | boolean | no |  |
| `address.unit` | string | no |  |
| `externalData.externalData[]` | array | no |  |
| `externalData.externalData[].key` | string | no |  |
| `vendorContacts[].email` | string | no |  |
| `address.city` | string | no |  |
| `memo` | string | no |  |
| `address.state` | string | no |  |
| `firstName` | string | no |  |
| `address.zip` | string | no |  |
| `lastName` | string | no |  |
| `address.country` | string | no |  |
| `phone` | string | no |  |
| `email` | string | no |  |
| `fax` | string | no |  |
| `externalData` | object | no |  |
| `isTruckReplenishment` | string | no |  |
| `taxRate` | number | no |  |
| `restrictedMobileCreation` | boolean | no |  |
| `vendorQuickbooksItem` | string | no |  |
| `paymentTermId` | number | no |  |
| `remittanceVendorId` | number | no |  |
| `address` | object | no |  |
| `id` | string | no |  |
| `vendorContacts[]` | array | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ServiceTitan API returns.

## Native endpoint

Through the native ServiceTitan API, this operation is `PATCH inventory/v2/tenant/{{credentials.tenant}}/vendors/:id` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-vendor.md) for the provider-specific parameters and requirements.

