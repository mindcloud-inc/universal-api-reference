# Create Product with TikTok Shop

## Endpoint

- **Method:** `POST`
- **Path:** `/product/202309/products`
- **Base URL:** `https://open-api.tiktokglobalshop.com/`
- **Official documentation:** [Create Product](https://partner.us.tiktokshop.com/dev/api-testing-tool?apiId=7262710099251201798&pkgId=431492&versionId=202309)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `save_mode` | body | `string` | no | Indicates how the product should be saved. Possible values: - AS_DRAFT: Save the product as a draft for future editing. - LISTING: Immediately list the product in the shop. Default: LISTING |
| `description` | body | `string` | yes | The product description in HTML format. **Note**: - The content must conform to the [HTML syntax](https://html.spec.whatwg.org/). All HTML tags are accepted but to optimize display on the TikTok Shop product detail page, the system will automatically convert certain tags into alternative formats, such as rendering `<table>` tags as images. - Max length: 10,000 characters. - Image guidelines: You must use [TikTok Shop image URLs](6509df95defece02be598a22). Max 30 `<img>` tags, each under 4000px with `src`, `width`, and `height` attributes. **Recommendations**: - If you are syncing a pre-existing description from another platform, include the full HTML source description here. - Provide a detailed description, ideally over 300 characters. - Include 3-5 key selling points, each under 250 characters, with supporting images. - Use 1600x1600 px for the image dimensions. |
| `category_id` | body | `string` | yes | — |
| `main_images` | body | `list<string>` | yes | A list of images to display in the product image gallery. - Max count: 9 - Arrange your image URIs in the sequence that they should appear on TikTok Shop. - Image dimensions: [300x300 px, 4000x4000 px] **Recommendations**: - Use a minimum of 5 images. - The first image should have a white background. Use the [Optimize Images API](665692b35d39dc02deb49a97) to change the background to white. |
| `skus` | body | `list<list>` | no | Send multiple values as a string. |
| `size_chart` | body | `boolean` | no | — |
| `is_cod_allowed` | body | `boolean` | no | — |
| `package_dimensions` | body | `boolean` | no | — |
| `length` | body | `string` | no | — |
