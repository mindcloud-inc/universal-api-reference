# <img src="https://images.mindcloud.co/apps/icons/encodian_1777474065581.jpeg" alt="Encodian - Barcode logo" width="28" height="28"> Encodian - Barcode: Universal API

Create and read barcodes, QR codes, and Swiss QR codes using Encodian's Barcode API. File inputs are base64 strings; document reads may return an Operation ID for a follow-up status check.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/encodianBarcode/latest
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.encodian.com/product/flowr/
- **Vendor API docs:** https://api.apps-encodian.com/swagger/Barcode/swagger.json

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Barcode - Read Document Status](actions/barcode-read-document-status.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encodianBarcode/latest/actions/barcode-read-document-status?connectionId=$CONNECTION_ID&operationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Barcode Document Status

| Action | Method | Description |
| --- | --- | --- |
| [Barcode - Read Document Status](actions/barcode-read-document-status.md) | GET |  |

### Barcode Image

| Action | Method | Description |
| --- | --- | --- |
| [Barcode - Create](actions/barcode-create.md) | POST |  |

### Barcode Values

| Action | Method | Description |
| --- | --- | --- |
| [Barcode - Read from Document](actions/barcode-read-from-document.md) | GET |  |
| [Barcode - Read from Image](actions/barcode-read-from-image.md) | GET |  |

### Qr Code Document Status

| Action | Method | Description |
| --- | --- | --- |
| [QR Code - Read Document Status](actions/qr-code-read-document-status.md) | GET |  |

### Qr Code Image

| Action | Method | Description |
| --- | --- | --- |
| [QR Code - Create](actions/qr-code-create.md) | POST |  |

### Qr Code Values

| Action | Method | Description |
| --- | --- | --- |
| [QR Code - Read from Document](actions/qr-code-read-from-document.md) | GET |  |
| [QR Code - Read from Image](actions/qr-code-read-from-image.md) | GET |  |

### Swiss Qr Code Image

| Action | Method | Description |
| --- | --- | --- |
| [Swiss QR Code - Create](actions/swiss-qr-code-create.md) | POST |  |

### Swiss Qr Code Values

| Action | Method | Description |
| --- | --- | --- |
| [Swiss QR Code - Read from Document](actions/swiss-qr-code-read-from-document.md) | GET |  |
| [Swiss QR Code - Read from Image](actions/swiss-qr-code-read-from-image.md) | GET |  |

