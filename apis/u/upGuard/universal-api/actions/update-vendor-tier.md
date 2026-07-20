# UpGuard: Update Vendor Tier

Updates the tier for a vendor in UpGuard.

```
PUT https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/update-vendor-tier
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UpGuard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/update-vendor-tier" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "vendorPrimaryHostname": "Ava Chen",
  "tier": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/update-vendor-tier', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "vendorPrimaryHostname": "Ava Chen",
    "tier": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `vendorPrimaryHostname` | string | yes | The primary hostname of the vendor to update tier for. |
| `tier` | number | yes | The tier to assign to the vendor. Use zero to remove the tier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native UpGuard API returns.

## Native endpoint

Through the native UpGuard API, this operation is `PUT /vendor/tier` (base URL `https://cyber-risk.upguard.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-vendor-tier.md) for the provider-specific parameters and requirements.

