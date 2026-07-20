# Swiss QR Code - Create with Encodian - Barcode

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Barcodes/CreateSwissQrCode`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Swiss QR Code - Create](https://support.encodian.com/hc/en-gb/articles/22209145105052)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `imageFormat` | body | `string` | yes | Output image format of the Swiss QR code. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`. |
| `account` | body | `string` | yes | Creditor IBAN or account value for the Swiss QR code. |
| `currency` | body | `string` | yes | Payment currency. Accepted values: `0`, `1`. |
| `amount` | body | `number` | yes | Payment amount. |
| `reference` | body | `string` | yes | Swiss QR payment reference value. |
| `creditor` | body | `object` | yes | Creditor object containing name and address fields. |
| `debtor` | body | `object` | yes | Debtor object containing name and address fields. |
| `width` | body | `number` | no | Swiss QR code width in pixels. |
