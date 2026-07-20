# Aspire: Update Vendor



```
PUT https://connect.mindcloud.co/v1/universal/aspire/latest/actions/update-vendor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/update-vendor" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "VendorName": "Ava Chen",
  "Active": true,
  "VendorID": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aspire/latest/actions/update-vendor', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "VendorName": "Ava Chen",
    "Active": true,
    "VendorID": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `BranchID` | list<number> | no |  |
| `VendorName` | string | yes |  |
| `AccountingVendorID` | string | no |  |
| `BillingTerms` | string | no |  |
| `Active` | boolean | yes |  |
| `VendorID` | list<number> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "vendorID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `vendorID` | number |  |

## Native endpoint

Through the native Aspire API, this operation is `PUT Vendors` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-vendor.md) for the provider-specific parameters and requirements.

