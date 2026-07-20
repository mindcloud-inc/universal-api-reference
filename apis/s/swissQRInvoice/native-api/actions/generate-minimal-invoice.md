# Generate Minimal Invoice with Swiss QR Invoice

Creates a minimal Swiss QR invoice in Magic Heidi.

## Endpoint

- **Method:** `POST`
- **Path:** `/create_invoice_abstract_v1d`
- **Base URL:** `https://europe-west6-magic-heidi.cloudfunctions.net`
- **Official documentation:** [Generate Minimal Invoice](https://github.com/magic-heidi/swiss-invoice-qr-code-api#generate-a-minimal-invoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | yes | Invoice data object nested under the documented top-level `data` request field. Edit the example values as needed. |
