# TikTok Shop: Get Aftersale Eligibility



```
GET https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/get-aftersale-eligibility
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TikTok Shop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/get-aftersale-eligibility?connectionId=$CONNECTION_ID&orderId=string&shopCipher=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderId": "string",
  "shopCipher": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/get-aftersale-eligibility?${params}`, {
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
| `orderId` | string | yes |  |
| `shopCipher` | string | yes |  |
| `initiateAftersaleUser` | list<string> | no | One of: `BUYER`, `SELLER`. Default: `SELLER`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `requestTypes` | list<string> | no | One of: `CANCEL`, `REFUND`, `RETURN_AND_REFUND`. Accepts multiple values in one string, delimited by `,`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native TikTok Shop API returns.

## Native endpoint

Through the native TikTok Shop API, this operation is `GET /return_refund/202602/orders/:order_id/aftersale_eligibility` (base URL `https://open-api.tiktokglobalshop.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-aftersale-eligibility.md) for the provider-specific parameters and requirements.

