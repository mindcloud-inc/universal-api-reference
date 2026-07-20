# <img src="https://images.mindcloud.co/apps/icons/happy-scribe_1773852254761.png" alt="HappyScribe logo" width="28" height="28"> HappyScribe: Universal API

HappyScribe API integration for uploads, transcription orders, exports, translations, glossaries, and style guides.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/happyScribe/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.happyscribe.com
- **Vendor API docs:** https://dev.happyscribe.com/sections/product/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Signed URL](actions/get-signed-url.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/happyScribe/latest/actions/get-signed-url?connectionId=$CONNECTION_ID&filename=my_media.mp3" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### Export

| Action | Method | Description |
| --- | --- | --- |
| [Create Export](actions/create-export.md) | POST | Creates a new export in HappyScribe. |
| [Retrieve Export](actions/retrieve-export.md) | GET | Retrieves an export from HappyScribe. |

### Glossary

| Action | Method | Description |
| --- | --- | --- |
| [List Glossaries](actions/list-glossaries.md) | GET | Retrieves glossaries from HappyScribe. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Confirm Order](actions/confirm-order.md) | PUT | Confirms an order in HappyScribe. |
| [Create Transcription or Subtitling Order](actions/create-transcription-or-subtitling-order.md) | POST | Creates a transcription or subtitling order in HappyScribe. |
| [Create Translation Order](actions/create-translation-order.md) | POST | Creates a translation order in HappyScribe. |
| [Retrieve Order](actions/retrieve-order.md) | GET | Retrieves an order from HappyScribe. |

### Style Guide

| Action | Method | Description |
| --- | --- | --- |
| [List Style Guides](actions/list-style-guides.md) | GET | Retrieves style guides from HappyScribe. |

### Transcription

| Action | Method | Description |
| --- | --- | --- |
| [Delete Transcription](actions/delete-transcription.md) | DELETE | Deletes a transcription from HappyScribe. |
| [List Transcriptions](actions/list-transcriptions.md) | GET | Retrieves transcriptions from HappyScribe. |
| [Retrieve Transcription](actions/retrieve-transcription.md) | GET | Retrieves a transcription from HappyScribe. |

### Upload

| Action | Method | Description |
| --- | --- | --- |
| [Get Signed URL](actions/get-signed-url.md) | GET | Retrieves a signed upload URL from HappyScribe. |

