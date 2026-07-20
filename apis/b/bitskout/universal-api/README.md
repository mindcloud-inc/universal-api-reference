# <img src="https://images.mindcloud.co/apps/icons/bitskout_1774878283603.png" alt="Bitskout logo" width="28" height="28"> Bitskout: Universal API

Extract data from documents, emails, and text with AI plugins

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bitskout/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.bitskout.com
- **Vendor API docs:** https://learn.microsoft.com/en-us/connectors/bitskout/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Plugins](actions/list-plugins.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bitskout/latest/actions/list-plugins?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Barcode Extraction

| Action | Method | Description |
| --- | --- | --- |
| [Extract Barcode from File](actions/extract-barcode-from-file.md) | POST | Extracts barcode values from a file with Bitskout. |

### Bill Of Lading Extraction

| Action | Method | Description |
| --- | --- | --- |
| [Extract Data from Bill of Lading](actions/extract-data-from-bill-of-lading.md) | POST | Extracts bill of lading data with a Bitskout plugin. |

### Business Card Extraction

| Action | Method | Description |
| --- | --- | --- |
| [Extract Data from Business Cards](actions/extract-data-from-business-cards.md) | POST | Extracts business card data with a Bitskout plugin. |

### Cold Email Response Detection

| Action | Method | Description |
| --- | --- | --- |
| [Detect Response to Cold Email](actions/detect-response-to-cold-email.md) | POST | Detects responses to cold emails with Bitskout. |

### Document Type Detection

| Action | Method | Description |
| --- | --- | --- |
| [Detect Document Type](actions/detect-document-type.md) | POST | Detects a document type with Bitskout. |

### Haro Query Extraction

| Action | Method | Description |
| --- | --- | --- |
| [Extract Data from HARO Query](actions/extract-data-from-haro-query.md) | POST | Extracts HARO query data with a Bitskout plugin. |

### Invoice Extraction

| Action | Method | Description |
| --- | --- | --- |
| [Extract Data from Invoice](actions/extract-data-from-invoice.md) | POST | Extracts invoice data with a Bitskout plugin. |

### Plugin

| Action | Method | Description |
| --- | --- | --- |
| [List Plugins](actions/list-plugins.md) | GET | Retrieves the available plugins from Bitskout. |

### Plugin Run

| Action | Method | Description |
| --- | --- | --- |
| [Run Plugin for File](actions/run-plugin-for-file.md) | POST | Runs a Bitskout plugin on a file. |
| [Run Plugin for Text](actions/run-plugin-for-text.md) | POST | Runs a Bitskout plugin on text. |

### Purchase Order Extraction

| Action | Method | Description |
| --- | --- | --- |
| [Extract Data from Purchase Order](actions/extract-data-from-purchase-order.md) | POST | Extracts purchase order data with a Bitskout plugin. |

### Qr Code Extraction

| Action | Method | Description |
| --- | --- | --- |
| [Extract QR Code from Document](actions/extract-qr-code-from-document.md) | POST | Extracts QR code values from a document with Bitskout. |

### Resume Extraction

| Action | Method | Description |
| --- | --- | --- |
| [Extract Data from CV](actions/extract-data-from-cv.md) | POST | Extracts CV data with a Bitskout plugin. |

