# <img src="https://images.mindcloud.co/apps/icons/open-qr_1777569484865.png" alt="OpenQR logo" width="28" height="28"> OpenQR: Universal API

Create, manage, and analyze QR codes

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/openQR/latest
- **Category:** Marketing
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://openqr.io/
- **Vendor API docs:** https://docs.openqr.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Files](actions/list-files.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openQR/latest/actions/list-files?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### File

| Action | Method | Description |
| --- | --- | --- |
| [List Files](actions/list-files.md) | GET | Lists QR logo files in the OpenQR account. |
| [Upload File](actions/upload-file.md) | POST | Uploads a file to the OpenQR account. |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST | Creates a new folder in OpenQR. |
| [List Folders](actions/list-folders.md) | GET | Lists folders in the OpenQR account. |
| [Update Folder](actions/update-folder.md) | PUT | Updates an existing folder in OpenQR. |

### Qr Code

| Action | Method | Description |
| --- | --- | --- |
| [Create Call QR Code](actions/create-call-qr-code.md) | POST | Creates a call QR code in OpenQR. |
| [Create Static Text QR Code](actions/create-static-text-qr-code.md) | POST | Creates a static text QR code in OpenQR. |
| [Create Static URL QR Code](actions/create-static-url-qr-code.md) | POST | Creates a static URL QR code in OpenQR. |
| [Create Text QR Code](actions/create-text-qr-code.md) | POST | Creates a text QR code in OpenQR. |
| [Create URL QR Code](actions/create-url-qr-code.md) | POST | Creates a URL QR code in OpenQR. |
| [Get QR Code](actions/get-qr-code.md) | GET | Retrieves a QR code from the OpenQR account. |
| [List QR Codes](actions/list-qr-codes.md) | GET | Lists QR codes in the OpenQR account. |
| [Update QR Code](actions/update-qr-code.md) | PUT | Updates an existing QR code in OpenQR. |

