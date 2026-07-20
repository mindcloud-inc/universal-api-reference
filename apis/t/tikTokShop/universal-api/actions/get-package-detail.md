# TikTok Shop: Get Package Detail

Returns information about a package, including handover time slot, tracking number, and shipping provider information.

```
GET https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/get-package-detail
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TikTok Shop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/get-package-detail?connectionId=$CONNECTION_ID&packageID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "packageID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/get-package-detail?${params}`, {
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
| `packageID` | string | yes |  |
| `shopCipher` | list<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "create_time": "2026-05-07T12:00:00.000Z",
      "delivery_option_id": "string",
      "delivery_option_name": "Ava Chen",
      "dimension": {
        "height": "string",
        "length": "string",
        "unit": "string",
        "width": "string"
      },
      "handover_method": "string",
      "has_multi_skus": true,
      "insurance": {
        "claim_status": "string",
        "coverage_amount": "string",
        "is_claim_eligible": true,
        "is_purchased": true
      },
      "last_mile_tracking_number": "string",
      "note_tag": "string",
      "order_line_item_ids": [
        "string"
      ],
      "orders": {
        "id": "string",
        "skus": {
          "id": "string",
          "image_url": "https://example.com",
          "name": "Ava Chen",
          "quantity": 1
        }
      },
      "package_id": "string",
      "package_status": "string",
      "pickup_slot": {
        "end_time": "2026-05-07T12:00:00.000Z",
        "start_time": "2026-05-07T12:00:00.000Z"
      },
      "recipient_address": {
        "address_detail": "string",
        "address_line1": "string",
        "address_line2": "string",
        "full_address": "string",
        "name": "Ava Chen",
        "phone_number": "string",
        "postal_code": "string",
        "region_code": "string"
      },
      "sender_address": {
        "full_address": "string",
        "name": "Ava Chen",
        "phone_number": "string",
        "postal_code": "string"
      },
      "shipping_provider_id": "string",
      "shipping_provider_name": "Ava Chen",
      "shipping_type": "string",
      "split_and_combine_tag": "string",
      "tracking_number": "string",
      "update_time": "2026-05-07T12:00:00.000Z",
      "weight": {
        "unit": "string",
        "value": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `create_time` | date |  |
| `delivery_option_id` | string |  |
| `delivery_option_name` | string |  |
| `dimension` | object |  |
| `dimension.height` | string |  |
| `dimension.length` | string |  |
| `dimension.unit` | string |  |
| `dimension.width` | string |  |
| `handover_method` | string |  |
| `has_multi_skus` | boolean |  |
| `insurance` | object |  |
| `insurance.claim_status` | string |  |
| `insurance.coverage_amount` | string |  |
| `insurance.is_claim_eligible` | boolean |  |
| `insurance.is_purchased` | boolean |  |
| `last_mile_tracking_number` | string |  |
| `note_tag` | string |  |
| `order_line_item_ids` | array |  |
| `orders` | array |  |
| `orders.id` | string |  |
| `orders.skus` | array |  |
| `orders.skus.id` | string |  |
| `orders.skus.image_url` | string |  |
| `orders.skus.name` | string |  |
| `orders.skus.quantity` | number |  |
| `package_id` | string |  |
| `package_status` | string |  |
| `pickup_slot` | object |  |
| `pickup_slot.end_time` | date |  |
| `pickup_slot.start_time` | date |  |
| `recipient_address` | object |  |
| `recipient_address.address_detail` | string |  |
| `recipient_address.address_line1` | string |  |
| `recipient_address.address_line2` | string |  |
| `recipient_address.full_address` | string |  |
| `recipient_address.name` | string |  |
| `recipient_address.phone_number` | string |  |
| `recipient_address.postal_code` | string |  |
| `recipient_address.region_code` | string |  |
| `sender_address` | object |  |
| `sender_address.full_address` | string |  |
| `sender_address.name` | string |  |
| `sender_address.phone_number` | string |  |
| `sender_address.postal_code` | string |  |
| `shipping_provider_id` | string |  |
| `shipping_provider_name` | string |  |
| `shipping_type` | string |  |
| `split_and_combine_tag` | string |  |
| `tracking_number` | string |  |
| `update_time` | date |  |
| `weight` | object |  |
| `weight.unit` | string |  |
| `weight.value` | string |  |

## Native endpoint

Through the native TikTok Shop API, this operation is `GET fulfillment/202309/packages/:packageID` (base URL `https://open-api.tiktokglobalshop.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-package-detail.md) for the provider-specific parameters and requirements.

