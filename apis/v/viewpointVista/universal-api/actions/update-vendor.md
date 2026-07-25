# Viewpoint Vista: Update Vendor



```
PUT https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/update-vendor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewpoint Vista `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/update-vendor" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "__key": {},
  "APCo": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/update-vendor', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "__key": {},
    "APCo": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `__key` | object | yes | "__key": { "KeyID": 5 }, |
| `__key.KeyID` | number | no |  |
| `PaymentAddress.Address` | string | no |  |
| `APCo` | number | yes |  |
| `PaymentAddress.Address2` | string | no |  |
| `PaymentAddress.City` | string | no |  |
| `SortName` | string | no |  |
| `Name` | string | no |  |
| `PaymentAddress.State` | string | no |  |
| `PaymentAddress.Zip` | string | no |  |
| `Type` | string | no |  |
| `PaymentAddress` | object | no |  |
| `PaymentAddress.Country` | string | no |  |
| `PaymentAddress.AddnlInfo` | string | no |  |
| `PurchasingAddress` | object | no |  |
| `PayTerms` | string | no |  |
| `CompanyContact` | object | no |  |
| `PayTerms` | string | no |  |
| `__custom_fields` | object | no | "__custom_fields": { "newKey": "New Value", "newKey-1": "New Value" } |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Viewpoint Vista API returns.

## Native endpoint

Through the native Viewpoint Vista API, this operation is `POST v1/direct/subscribers/:subscriber_code/vista/:api/2/data/vendors/actions/change` (base URL `https://api.xchange.trimble.com/connect/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-vendor.md) for the provider-specific parameters and requirements.

