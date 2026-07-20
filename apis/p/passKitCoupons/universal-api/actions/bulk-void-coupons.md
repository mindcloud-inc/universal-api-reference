# PassKit Coupons: Bulk Void Coupons



```
DELETE https://connect.mindcloud.co/v1/universal/passKitCoupons/latest/actions/bulk-void-coupons
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PassKit Coupons `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/passKitCoupons/latest/actions/bulk-void-coupons?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/passKitCoupons/latest/actions/bulk-void-coupons?${params}`, {
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
| `classId` | string | no | Coupon campaign ID for the bulk void scope. |
| `protocol` | string | no | Pass protocol for the bulk void request. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PassKit Coupons API returns.

## Native endpoint

Through the native PassKit Coupons API, this operation is `DELETE /coupon/singleUse/coupons/bulk` (base URL `https://api.pub2.passkit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-void-coupons.md) for the provider-specific parameters and requirements.

