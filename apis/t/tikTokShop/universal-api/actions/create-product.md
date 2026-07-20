# TikTok Shop: Create Product



```
POST https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/create-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TikTok Shop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/create-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "description": "string",
  "category_id": "string",
  "main_images": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/create-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "description": "string",
    "category_id": "string",
    "main_images": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `save_mode` | string | no | Indicates how the product should be saved. Possible values: - AS_DRAFT: Save the product as a draft for future editing. - LISTING: Immediately list the product in the shop. Default: LISTING |
| `description` | string | yes | The product description in HTML format. **Note**: - The content must conform to the [HTML syntax](https://html.spec.whatwg.org/). All HTML tags are accepted but to optimize display on the TikTok Shop product detail page, the system will automatically convert certain tags into alternative formats, such as rendering `<table>` tags as images. - Max length: 10,000 characters. - Image guidelines: You must use [TikTok Shop image URLs](6509df95defece02be598a22). Max 30 `<img>` tags, each under 4000px with `src`, `width`, and `height` attributes. **Recommendations**: - If you are syncing a pre-existing description from another platform, include the full HTML source description here. - Provide a detailed description, ideally over 300 characters. - Include 3-5 key selling points, each under 250 characters, with supporting images. - Use 1600x1600 px for the image dimensions. |
| `category_id` | string | yes |  |
| `main_images` | list<string> | yes | A list of images to display in the product image gallery. - Max count: 9 - Arrange your image URIs in the sequence that they should appear on TikTok Shop. - Image dimensions: [300x300 px, 4000x4000 px] **Recommendations**: - Use a minimum of 5 images. - The first image should have a white background. Use the [Optimize Images API](665692b35d39dc02deb49a97) to change the background to white. |
| `skus` | list<list> | no | Accepts multiple values in one string. |
| `size_chart` | boolean | no |  |
| `is_cod_allowed` | boolean | no |  |
| `package_dimensions` | boolean | no |  |
| `length` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native TikTok Shop API returns.

## Native endpoint

Through the native TikTok Shop API, this operation is `POST /product/202309/products` (base URL `https://open-api.tiktokglobalshop.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product.md) for the provider-specific parameters and requirements.

