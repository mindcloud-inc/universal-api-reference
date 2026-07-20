# Vouchery.io: Create Voucher



```
POST https://connect.mindcloud.co/v1/universal/voucheryio/latest/actions/create-voucher
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vouchery.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/voucheryio/latest/actions/create-voucher" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": 1,
  "code": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voucheryio/latest/actions/create-voucher', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": 1,
    "code": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | number | yes | Campaign ID from the path. |
| `code` | string | yes | Voucher code to create. |
| `customerIdentifier` | string | no | Optional customer identifier to assign the voucher. |
| `giftCardValue` | number | no | Optional gift card value for gift card vouchers. |
| `activatesAt` | string | no | Optional activation timestamp. |
| `voucherValidUntil` | string | no | Optional voucher expiration timestamp. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Vouchery.io API returns.

## Native endpoint

Through the native Vouchery.io API, this operation is `POST /campaigns/:campaign_id/vouchers` (base URL `https://mindcloud.sandbox.vouchery.app/api/v2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-voucher.md) for the provider-specific parameters and requirements.

