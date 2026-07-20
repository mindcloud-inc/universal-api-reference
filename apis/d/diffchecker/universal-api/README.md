# <img src="https://images.mindcloud.co/apps/icons/screenshot-2026-03-31-154137_1774982541075.png" alt="Diffchecker logo" width="28" height="28"> Diffchecker: Universal API

Diffchecker compares text, PDF documents, images, and spreadsheets through a REST API with JSON, HTML, and image-based diff outputs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/diffchecker/latest
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.diffchecker.com
- **Vendor API docs:** https://www.diffchecker.com/docs/getting-started/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Test Authentication](actions/test-authentication.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/diffchecker/latest/actions/test-authentication?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Authentication

| Action | Method | Description |
| --- | --- | --- |
| [Test Authentication](actions/test-authentication.md) | GET | Tests Diffchecker API authentication with the current API key. |

### Image Diff

| Action | Method | Description |
| --- | --- | --- |
| [Compare Images (JSON, Data URLs)](actions/compare-images-json-data-urls.md) | GET | Compares images in Diffchecker and returns a JSON diff from data URLs. |
| [Compare Images (JSON, Uploads)](actions/compare-images-json-uploads.md) | GET | Compares images in Diffchecker and returns a JSON diff from uploads. |

### Pdf Diff

| Action | Method | Description |
| --- | --- | --- |
| [Compare Documents (HTML JSON, Character, Data URLs)](actions/compare-documents-html-json-character-data-urls.md) | GET | Compares documents in Diffchecker and returns a character-level HTML JSON diff from data URLs. |
| [Compare Documents (HTML JSON, Character, Uploads)](actions/compare-documents-html-json-character-uploads.md) | GET | Compares documents in Diffchecker and returns a character-level HTML JSON diff from uploads. |
| [Compare Documents (HTML JSON, Data URLs)](actions/compare-documents-html-json-data-urls.md) | GET | Compares documents in Diffchecker and returns an HTML JSON diff from data URLs. |
| [Compare Documents (HTML JSON, Default Word, Data URLs)](actions/compare-documents-html-json-default-word-data-urls.md) | GET | Compares documents in Diffchecker and returns a word-level HTML JSON diff from data URLs. |
| [Compare Documents (HTML JSON, Default Word, Uploads)](actions/compare-documents-html-json-default-word-uploads.md) | GET | Compares documents in Diffchecker and returns a word-level HTML JSON diff from uploads. |
| [Compare Documents (HTML JSON, Uploads)](actions/compare-documents-html-json-uploads.md) | GET | Compares documents in Diffchecker and returns an HTML JSON diff from uploads. |
| [Compare Documents (JSON, Character, Data URLs)](actions/compare-documents-json-character-data-urls.md) | GET | Compares documents in Diffchecker and returns a character-level JSON diff from data URLs. |
| [Compare Documents (JSON, Character, Uploads)](actions/compare-documents-json-character-uploads.md) | GET | Compares documents in Diffchecker and returns a character-level JSON diff from uploads. |
| [Compare Documents (JSON, Data URLs)](actions/compare-documents-json-data-urls.md) | GET | Compares documents in Diffchecker and returns a JSON diff from data URLs. |
| [Compare Documents (JSON, Default Word, Data URLs)](actions/compare-documents-json-default-word-data-urls.md) | GET | Compares documents in Diffchecker and returns a word-level JSON diff from data URLs. |
| [Compare Documents (JSON, Default Word, Uploads)](actions/compare-documents-json-default-word-uploads.md) | GET | Compares documents in Diffchecker and returns a word-level JSON diff from uploads. |
| [Compare Documents (JSON, Uploads)](actions/compare-documents-json-uploads.md) | GET | Compares documents in Diffchecker and returns a JSON diff from uploads. |

### Spreadsheet Diff

| Action | Method | Description |
| --- | --- | --- |
| [Compare Excel Spreadsheets (Formulas, Data URLs)](actions/compare-excel-spreadsheets-formulas-data-urls.md) | GET | Compares Excel spreadsheets in Diffchecker using formulas from data URLs. |
| [Compare Excel Spreadsheets (Formulas, Normalized, Data URLs)](actions/compare-excel-spreadsheets-formulas-normalized-data-urls.md) | GET | Compares Excel spreadsheets in Diffchecker using normalized formulas from data URLs. |
| [Compare Excel Spreadsheets (Formulas, Normalized, Uploads)](actions/compare-excel-spreadsheets-formulas-normalized-uploads.md) | GET | Compares Excel spreadsheets in Diffchecker using normalized formulas from uploads. |
| [Compare Excel Spreadsheets (Formulas, Uploads)](actions/compare-excel-spreadsheets-formulas-uploads.md) | GET | Compares Excel spreadsheets in Diffchecker using formulas from uploads. |
| [Compare Excel Spreadsheets (Standard, Data URLs)](actions/compare-excel-spreadsheets-standard-data-urls.md) | GET | Compares Excel spreadsheets in Diffchecker using standard values from data URLs. |
| [Compare Excel Spreadsheets (Standard, Hide Unchanged, Data URLs)](actions/compare-excel-spreadsheets-standard-hide-unchanged-data-urls.md) | GET | Compares Excel spreadsheets in Diffchecker hiding unchanged rows and columns from data URLs. |
| [Compare Excel Spreadsheets (Standard, Normalized, Data URLs)](actions/compare-excel-spreadsheets-standard-normalized-data-urls.md) | GET | Compares Excel spreadsheets in Diffchecker using normalized standard values from data URLs. |
| [Compare Excel Spreadsheets (Standard, Normalized, Uploads)](actions/compare-excel-spreadsheets-standard-normalized-uploads.md) | GET | Compares Excel spreadsheets in Diffchecker using normalized standard values from uploads. |
| [Compare Excel Spreadsheets (Standard, Uploads)](actions/compare-excel-spreadsheets-standard-uploads.md) | GET | Compares Excel spreadsheets in Diffchecker using standard values from uploads. |

### Text Diff

| Action | Method | Description |
| --- | --- | --- |
| [Compare Text (HTML JSON)](actions/compare-text-html-json.md) | GET | Compares text in Diffchecker and returns an HTML JSON diff. |
| [Compare Text (HTML JSON, Character)](actions/compare-text-html-json-character.md) | GET | Compares text in Diffchecker and returns a character-level HTML JSON diff. |
| [Compare Text (HTML JSON, Default Word)](actions/compare-text-html-json-default-word.md) | GET | Compares text in Diffchecker and returns a word-level HTML JSON diff. |
| [Compare Text (JSON)](actions/compare-text-json.md) | GET | Compares text in Diffchecker and returns a JSON diff. |
| [Compare Text (JSON, Character)](actions/compare-text-json-character.md) | GET | Compares text in Diffchecker and returns a character-level JSON diff. |
| [Compare Text (JSON, Default Word)](actions/compare-text-json-default-word.md) | GET | Compares text in Diffchecker and returns a word-level JSON diff. |

