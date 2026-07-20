# <img src="https://images.mindcloud.co/apps/icons/favicon-32x32_1776820713283.png" alt="Memix logo" width="28" height="28"> Memix: Universal API

Search templates and generate memes, GIFs, and previews

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/memix/latest
- **Actions:** 17
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.memix.com
- **Vendor API docs:** https://api.memix.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Generate GIF Memix](actions/generate-gif-memix.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/memix/latest/actions/generate-gif-memix?connectionId=$CONNECTION_ID&template_slug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (17)

### Memix Gif

| Action | Method | Description |
| --- | --- | --- |
| [Generate GIF Memix](actions/generate-gif-memix.md) | GET | Retrieves a generated GIF from Memix. |

### Memix Jpeg

| Action | Method | Description |
| --- | --- | --- |
| [Generate JPEG Memix](actions/generate-jpeg-memix.md) | GET | Retrieves a generated JPEG from Memix. |

### Memix Mp4

| Action | Method | Description |
| --- | --- | --- |
| [Generate MP4 Memix](actions/generate-mp4-memix.md) | GET | Retrieves a generated MP4 from Memix. |

### Memix Preview Gif

| Action | Method | Description |
| --- | --- | --- |
| [Preview GIF Memix](actions/preview-gif-memix.md) | GET | Retrieves a GIF preview from Memix. |

### Memix Preview Jpeg

| Action | Method | Description |
| --- | --- | --- |
| [Preview JPEG Memix](actions/preview-jpeg-memix.md) | GET | Retrieves a JPEG preview from Memix. |

### Memix Preview Mp4

| Action | Method | Description |
| --- | --- | --- |
| [Preview MP4 Memix](actions/preview-mp4-memix.md) | GET | Retrieves an MP4 preview from Memix. |

### Memix Preview Webp

| Action | Method | Description |
| --- | --- | --- |
| [Preview WebP Memix](actions/preview-web-p-memix.md) | GET | Retrieves a WebP preview from Memix. |

### Memix Webp

| Action | Method | Description |
| --- | --- | --- |
| [Generate WebP Memix](actions/generate-web-p-memix.md) | GET | Retrieves a generated WebP from Memix. |

### Referral Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Referrals Status](actions/get-referrals-status.md) | GET | Retrieves current referral status from Memix. |

### Subscription Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Subscription Status](actions/get-subscription-status.md) | GET | Retrieves current subscription status from Memix. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Get All Templates](actions/get-all-templates.md) | GET | Retrieves all available templates from Memix. |
| [Get Template Details](actions/get-template-details.md) | GET | Retrieves full template details from Memix. |
| [Search Curated Templates](actions/search-curated-templates.md) | GET | Finds curated templates in Memix search. |
| [Search Templates By Image URL](actions/search-templates-by-image-url.md) | GET | Finds templates in Memix by image URL. |
| [Search Templates By Query](actions/search-templates-by-query.md) | GET | Finds templates in Memix by query. |
| [Search Templates By Text](actions/search-templates-by-text.md) | GET | Finds templates in Memix by text. |

### Template Shortcut

| Action | Method | Description |
| --- | --- | --- |
| [Get Template Shortcuts](actions/get-template-shortcuts.md) | GET | Retrieves available template shortcuts from Memix. |

