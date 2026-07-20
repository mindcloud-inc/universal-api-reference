# UpGuard: Update Vendor Attributes

Updates attributes for a vendor in UpGuard.

```
PUT https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/update-vendor-attributes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UpGuard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/update-vendor-attributes" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "vendorPrimaryHostname": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/update-vendor-attributes', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "vendorPrimaryHostname": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `vendorPrimaryHostname` | string | yes | The primary hostname of the vendor to update attributes for. |
| `attributes` | object | no | Attributes to assign to the vendor. Use null to reset an attribute value. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native UpGuard API returns.

## Native endpoint

Through the native UpGuard API, this operation is `PUT /vendor/attributes` (base URL `https://cyber-risk.upguard.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-vendor-attributes.md) for the provider-specific parameters and requirements.

