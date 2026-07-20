# <img src="https://images.mindcloud.co/apps/icons/geral_1776106463698.png" alt="Geral logo" width="28" height="28"> Geral: Universal API

Manage links, QR codes, analytics, and custom domains

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/geral/latest
- **Category:** Marketing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://ger.al/
- **Vendor API docs:** https://ger.al/api-documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User](actions/get-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/geral/latest/actions/get-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Account Log

| Action | Method | Description |
| --- | --- | --- |
| [List Account Logs](actions/list-account-logs.md) | GET | Retrieves account logs from Geral. |

### Collected Data

| Action | Method | Description |
| --- | --- | --- |
| [Get Collected Data](actions/get-collected-data.md) | GET | Retrieves collected data from Geral by ID. |
| [List Collected Data](actions/list-collected-data.md) | GET | Retrieves collected data from Geral. |

### Domain

| Action | Method | Description |
| --- | --- | --- |
| [Delete Domain](actions/delete-domain.md) | DELETE | Deletes a custom domain from Geral. |
| [Get Domain](actions/get-domain.md) | GET | Retrieves a custom domain from Geral by ID. |
| [List Domains](actions/list-domains.md) | GET | Retrieves custom domains from Geral. |

### Link

| Action | Method | Description |
| --- | --- | --- |
| [Delete Link](actions/delete-link.md) | DELETE | Deletes a link from Geral. |
| [Get Link](actions/get-link.md) | GET | Retrieves a link from Geral by ID. |
| [List Links](actions/list-links.md) | GET | Retrieves links from Geral. |

### Notification Handler

| Action | Method | Description |
| --- | --- | --- |
| [Get Notification Handler](actions/get-notification-handler.md) | GET | Retrieves a notification handler from Geral by ID. |
| [List Notification Handlers](actions/list-notification-handlers.md) | GET | Retrieves notification handlers from Geral. |

### Payment

| Action | Method | Description |
| --- | --- | --- |
| [Get Payment](actions/get-payment.md) | GET | Retrieves an account payment from Geral by ID. |
| [List Payments](actions/list-payments.md) | GET | Retrieves account payments from Geral. |

### Pixel

| Action | Method | Description |
| --- | --- | --- |
| [Delete Pixel](actions/delete-pixel.md) | DELETE | Deletes a pixel from Geral. |
| [Get Pixel](actions/get-pixel.md) | GET | Retrieves a pixel from Geral by ID. |
| [List Pixels](actions/list-pixels.md) | GET | Retrieves pixels from Geral. |

### Qr Code

| Action | Method | Description |
| --- | --- | --- |
| [Delete QR Code](actions/delete-qr-code.md) | DELETE | Deletes a QR code from Geral. |
| [Get QR Code](actions/get-qr-code.md) | GET | Retrieves a QR code from Geral by ID. |
| [List QR Codes](actions/list-qr-codes.md) | GET | Retrieves QR codes from Geral. |

### Splash Page

| Action | Method | Description |
| --- | --- | --- |
| [Get Splash Page](actions/get-splash-page.md) | GET | Retrieves a splash page from Geral by ID. |
| [List Splash Pages](actions/list-splash-pages.md) | GET | Retrieves splash pages from Geral. |

### Statistic

| Action | Method | Description |
| --- | --- | --- |
| [Get Link Statistics](actions/get-link-statistics.md) | GET | Retrieves statistics for a link in Geral. |
| [List Statistics](actions/list-statistics.md) | GET | Retrieves account statistics from Geral. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves the current user from Geral. |

