# <img src="https://images.mindcloud.co/apps/icons/t-lylink-shortener_1774893557564.png" alt="TLY Link Shortener logo" width="28" height="28"> TLY Link Shortener: Universal API

Create, manage, and analyze shortened links, tags, pixels, QR codes, OneLinks, and UTM presets in T.LY.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/tLYLinkShortener/latest
- **Category:** Marketing
- **Actions:** 29
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://t.ly/
- **Vendor API docs:** https://t.ly/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Short Links](actions/list-short-links.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tLYLinkShortener/latest/actions/list-short-links?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (29)

### Onelink

| Action | Method | Description |
| --- | --- | --- |
| [List OneLinks](actions/list-one-links.md) | GET | Retrieves OneLinks from TLY Link Shortener. |

### Onelink Stats

| Action | Method | Description |
| --- | --- | --- |
| [Delete OneLink Stats](actions/delete-one-link-stats.md) | DELETE | Deletes stats for a OneLink in TLY Link Shortener. |
| [Get OneLink Stats](actions/get-one-link-stats.md) | GET | Retrieves stats for a OneLink in TLY Link Shortener. |

### Pixel

| Action | Method | Description |
| --- | --- | --- |
| [Create Pixel](actions/create-pixel.md) | POST | Creates a new pixel in TLY Link Shortener. |
| [Delete Pixel](actions/delete-pixel.md) | DELETE | Deletes an existing pixel from TLY Link Shortener. |
| [Get Pixel](actions/get-pixel.md) | GET | Retrieves a pixel from TLY Link Shortener. |
| [List Pixels](actions/list-pixels.md) | GET | Retrieves pixels from TLY Link Shortener. |
| [Update Pixel](actions/update-pixel.md) | PUT | Updates an existing pixel in TLY Link Shortener. |

### Qr Code

| Action | Method | Description |
| --- | --- | --- |
| [Get QR Code](actions/get-qr-code.md) | GET | Retrieves a QR code from TLY Link Shortener. |
| [Update QR Code](actions/update-qr-code.md) | PUT | Updates a QR code in TLY Link Shortener. |

### Short Link

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Shorten Links](actions/bulk-shorten-links.md) | POST | Creates short links in bulk in TLY Link Shortener. |
| [Bulk Update Links](actions/bulk-update-links.md) | PUT | Updates short links in bulk in TLY Link Shortener. |
| [Create Short Link](actions/create-short-link.md) | POST | Creates a new short link in TLY Link Shortener. |
| [Delete Short Link](actions/delete-short-link.md) | DELETE | Deletes an existing short link from TLY Link Shortener. |
| [Expand Short Link](actions/expand-short-link.md) | GET | Expands a short link in TLY Link Shortener. |
| [Get Short Link](actions/get-short-link.md) | GET | Retrieves a short link from TLY Link Shortener. |
| [List Short Links](actions/list-short-links.md) | GET | Retrieves short links from TLY Link Shortener. |
| [Update Short Link](actions/update-short-link.md) | PUT | Updates an existing short link in TLY Link Shortener. |

### Short Link Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get Short Link Stats](actions/get-short-link-stats.md) | GET | Retrieves stats for a short link in TLY Link Shortener. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a new tag in TLY Link Shortener. |
| [Delete Tag](actions/delete-tag.md) | DELETE | Deletes an existing tag from TLY Link Shortener. |
| [Get Tag](actions/get-tag.md) | GET | Retrieves a tag from TLY Link Shortener. |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from TLY Link Shortener. |
| [Update Tag](actions/update-tag.md) | PUT | Updates an existing tag in TLY Link Shortener. |

### Utm Preset

| Action | Method | Description |
| --- | --- | --- |
| [Create UTM Preset](actions/create-utm-preset.md) | POST | Creates a new UTM preset in TLY Link Shortener. |
| [Delete UTM Preset](actions/delete-utm-preset.md) | DELETE | Deletes an existing UTM preset from TLY Link Shortener. |
| [Get UTM Preset](actions/get-utm-preset.md) | GET | Retrieves a UTM preset from TLY Link Shortener. |
| [List UTM Presets](actions/list-utm-presets.md) | GET | Retrieves UTM presets from TLY Link Shortener. |
| [Update UTM Preset](actions/update-utm-preset.md) | PUT | Updates an existing UTM preset in TLY Link Shortener. |

