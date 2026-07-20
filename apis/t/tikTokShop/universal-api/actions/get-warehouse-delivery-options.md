# TikTok Shop: Get Warehouse Delivery Options

This API is used to obtain a list of delivery options available through the seller's designated warehouse.

```
GET https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/get-warehouse-delivery-options
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TikTok Shop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/get-warehouse-delivery-options?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/get-warehouse-delivery-options?${params}`, {
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
| `warehouse_id` | string | no |  |
| `shopCipher` | list<string> | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native TikTok Shop API returns.

## Native endpoint

Through the native TikTok Shop API, this operation is `GET logistics/202309/warehouses/:warehouse_id/delivery_options` (base URL `https://open-api.tiktokglobalshop.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-warehouse-delivery-options.md) for the provider-specific parameters and requirements.

