# <img src="https://images.mindcloud.co/apps/icons/picsart_1775742909496.png" alt="Picsart logo" width="28" height="28"> Picsart: Universal API

Create, edit, and transform images with AI

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/picsart/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://picsart.io
- **Vendor API docs:** https://docs.picsart.io/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Credits Balance](actions/get-credits-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/picsart/latest/actions/get-credits-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Ai Effect

| Action | Method | Description |
| --- | --- | --- |
| [Get AI Effect Names](actions/get-ai-effect-names.md) | GET | Retrieves supported AI effect names from Picsart. |

### Background Removal

| Action | Method | Description |
| --- | --- | --- |
| [Remove Background](actions/remove-background.md) | POST | Creates a background-removed image in Picsart. |

### Blend

| Action | Method | Description |
| --- | --- | --- |
| [Blend Images](actions/blend-images.md) | POST | Creates a blended image in Picsart. |

### Color Transfer

| Action | Method | Description |
| --- | --- | --- |
| [Transfer Image Colors](actions/transfer-image-colors.md) | POST | Creates an image with transferred colors in Picsart. |

### Credits Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Credits Balance](actions/get-credits-balance.md) | GET | Retrieves your remaining Picsart credits balance. |

### Effect

| Action | Method | Description |
| --- | --- | --- |
| [Get Effect Names](actions/get-effect-names.md) | GET | Retrieves supported effect names from Picsart. |

### Image Adjustment

| Action | Method | Description |
| --- | --- | --- |
| [Adjust Image](actions/adjust-image.md) | POST | Creates an adjusted image in Picsart. |

### Image Edit

| Action | Method | Description |
| --- | --- | --- |
| [Edit Image](actions/edit-image.md) | POST | Creates an edited image in Picsart. |

### Style Transfer

| Action | Method | Description |
| --- | --- | --- |
| [Transfer Image Style](actions/transfer-image-style.md) | POST | Creates an image with transferred style in Picsart. |

### Upscale

| Action | Method | Description |
| --- | --- | --- |
| [Upscale Image](actions/upscale-image.md) | POST | Creates an upscaled image in Picsart. |

### Vectorizer

| Action | Method | Description |
| --- | --- | --- |
| [Vectorize Image](actions/vectorize-image.md) | POST | Creates an SVG image from a raster image in Picsart. |

