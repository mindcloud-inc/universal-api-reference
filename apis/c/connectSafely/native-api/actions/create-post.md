# Create a LinkedIn post with ConnectSafely

Publishes a LinkedIn post. The mediaType field decides what you post. Text (none): send text only, one call with no upload. Image (image): upload via /posts/upload/init, then pass assetUrn (and optional altText). Carousel (image): upload each image, then pass 2 to 9 of them in assetUrns. Video (video): upload, then pass assetUrn and recipes. Document/PDF (document): upload, poll /posts/upload/document-status until READY, then pass assetUrn, recipes, and title. New to the API? The step-by-step guide with cURL, JavaScript, and Python examples for each post type lives at /docs/api/posting. To publish as a company page you administer, pass companyUrn (the company URN).

## Endpoint

- **Method:** `POST`
- **Path:** `/posts/create`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Create a LinkedIn post](https://connectsafely.ai/docs/api/linkedin-posts/post-posts-create-create-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | Which connected account posts. Omit to use the default account. |
| `text` | body | `string` | yes | The post body (max 3,000 characters). |
| `visibility` | body | `list` | no | Who can see the post. Accepted values: `ANYONE`, `CONNECTIONS_ONLY`. Default: `ANYONE`. |
| `mediaType` | body | `list` | no | What you are posting. Use "image" for a carousel too (with assetUrns). Accepted values: `none`, `image`, `video`, `document`. Default: `none`. |
| `assetUrn` | body | `string` | no | Single uploaded asset from /posts/upload/init. Required for image / video / document (a single image, video, or PDF). |
| `assetUrns` | body | `array` | no | Carousel only: 2–9 uploaded images. Each item is { assetUrn, altText? }. Use instead of assetUrn with mediaType "image". |
| `recipes` | body | `array` | no | From /posts/upload/init. Required for video and document. |
| `altText` | body | `string` | no | Accessibility alt text for a single image (mediaType "image"). Default: ``. |
| `title` | body | `string` | no | Document title shown on the post (mediaType "document"). |
| `companyUrn` | body | `string` | no | Optional. Post as a company page you administer instead of your personal profile. Provide the company URN (e.g., "urn:li:fsd_company:105672170"). |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `postUrn` | `string` |  |
| `shareUrn` | `string` |  |
| `accountId` | `string` |  |
| `companyUrn` | `string` | Company URN the post was authored as (only present when posting as a company page). |

## Error status codes

`400`, `401`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
