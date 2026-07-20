# ServiceTitan: Add Vendor



```
POST https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/post-vendor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTitan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/post-vendor" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/post-vendor', {
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
| `address.street` | string | no |  |
| `externalData.applicationGuid` | string | no |  |
| `externalData.externalDataList[].key` | string | no |  |
| `name` | string | no |  |
| `tags][].tagTypeId` | number | no |  |
| `vendorContacts[].name` | string | no |  |
| `active` | boolean | no |  |
| `address.unit` | string | no |  |
| `externalData.externalDataList[]` | array | no |  |
| `externalData.externalDataList[].value` | string | no |  |
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
| `isTruckReplenishment` | boolean | no | Example: `False`. |
| `taxRate` | number | no |  |
| `restrictedMobileCreation` | boolean | no | Example: `False`. |
| `vendorQuickbooksItem` | string | no |  |
| `paymentTermId` | number | no |  |
| `remittanceVendorId` | number | no |  |
| `address` | object | no |  |
| `vendorContacts[]` | array | no |  |
| `externalData` | object | no |  |
| `deliveryOption` | string | no |  |
| `tags][]` | array | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ServiceTitan API returns.

## Native endpoint

Through the native ServiceTitan API, this operation is `POST inventory/v2/tenant/{{credentials.tenant}}/vendors` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-vendor.md) for the provider-specific parameters and requirements.

