# TikTok Shop: Get Shipping Providers

This API is used to obtain the shipping provider corresponding to the specified delivery option.

```
GET https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/get-shipping-providers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TikTok Shop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/get-shipping-providers?connectionId=$CONNECTION_ID&delivery_option_id=string&shopCipher=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "delivery_option_id": "string",
  "shopCipher": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/get-shipping-providers?${params}`, {
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
| `delivery_option_id` | string | yes |  |
| `shopCipher` | list<string> | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native TikTok Shop API returns.

## Native endpoint

Through the native TikTok Shop API, this operation is `GET logistics/202309/delivery_options/:delivery_option_id/shipping_providers` (base URL `https://open-api.tiktokglobalshop.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shipping-providers.md) for the provider-specific parameters and requirements.

