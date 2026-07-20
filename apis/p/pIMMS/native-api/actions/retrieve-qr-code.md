# Retrieve QR Code with PIMMS

Retrieves a QR code image from PIMMS.

## Endpoint

- **Method:** `GET`
- **Path:** `/qr`
- **Base URL:** `https://api.pimms.io`
- **Official documentation:** [Retrieve QR Code](https://pimms.apidocumentation.com/reference#tag/qr-codes/GET/qr)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | The URL to generate a QR code for. |
| `logo` | query | `string` | no | The logo to include in the QR code. Can only be used with a paid plan on PiMMs |
| `size` | query | `number` | no | The size of the QR code in pixels. Defaults to `600` if not provided. |
| `level` | query | `string` | no | The level of error correction to use for the QR code. Defaults to `L` if not provided. |
| `fgColor` | query | `string` | no | The foreground color of the QR code in hex format. Defaults to `#000000` if not provided. |
| `bgColor` | query | `string` | no | The background color of the QR code in hex format. Defaults to `#ffffff` if not provided. |
| `hideLogo` | query | `boolean` | no | Whether to hide the logo in the QR code. Can only be used with a paid plan on PiMMs. |
| `margin` | query | `number` | no | The size of the margin around the QR code. Defaults to 2 if not provided. |
| `includeMargin` | query | `boolean` | no | DEPRECATED: Margin is included by default. Use the `margin` prop to customize the margin size. |
