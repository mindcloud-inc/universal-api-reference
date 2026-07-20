# TikTok Shop: Get Package Shipping Document (v2)



```
GET https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/get-package-shipping-document-v2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TikTok Shop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/get-package-shipping-document-v2?connectionId=$CONNECTION_ID&document_type=string&package_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "document_type": "string",
  "package_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/get-package-shipping-document-v2?${params}`, {
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
| `shopCipher` | list<list> | no |  |
| `document_type` | string | yes |  |
| `document_size` | string | no |  |
| `document_format` | string | no |  |
| `package_id` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native TikTok Shop API returns.

## Native endpoint

Through the native TikTok Shop API, this operation is `GET /fulfillment/202309/packages/:package_id/shipping_documents` (base URL `https://open-api.tiktokglobalshop.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-package-shipping-document-v2.md) for the provider-specific parameters and requirements.

