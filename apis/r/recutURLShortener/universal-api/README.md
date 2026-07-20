# <img src="https://images.mindcloud.co/apps/icons/r-1_1776712233391.png" alt="Recut URL Shortener logo" width="28" height="28"> Recut URL Shortener: Universal API

Manage branded links, QR codes, and click tracking

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/recutURLShortener/latest
- **Category:** Marketing
- **Actions:** 35
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://recut.in
- **Vendor API docs:** https://app.recut.in/developers

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (35)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves account details from Recut URL Shortener. |
| [Update Account](actions/update-account.md) | PUT | Updates account details in Recut URL Shortener. |

### Branded Domain

| Action | Method | Description |
| --- | --- | --- |
| [Create Branded Domain](actions/create-branded-domain.md) | POST | Creates a branded domain in Recut URL Shortener. |
| [Delete Domain](actions/delete-domain.md) | DELETE | Deletes an existing branded domain from Recut URL Shortener. |
| [List Branded Domains](actions/list-branded-domains.md) | GET | Retrieves branded domains from Recut URL Shortener. |
| [Update Domain](actions/update-domain.md) | PUT | Updates an existing branded domain in Recut URL Shortener. |

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Assign Link To Campaign](actions/assign-link-to-campaign.md) | POST | Assigns a link to a campaign in Recut URL Shortener. |
| [Create Campaign](actions/create-campaign.md) | POST | Creates a campaign in Recut URL Shortener. |
| [Delete Campaign](actions/delete-campaign.md) | DELETE | Deletes an existing campaign from Recut URL Shortener. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaigns from Recut URL Shortener. |
| [Update Campaign](actions/update-campaign.md) | PUT | Updates an existing campaign in Recut URL Shortener. |

### Channels

| Action | Method | Description |
| --- | --- | --- |
| [Assign Item To Channel](actions/assign-item-to-channel.md) | POST | Assigns an item to a channel in Recut URL Shortener. |
| [Create Channel](actions/create-channel.md) | POST | Creates a channel in Recut URL Shortener. |
| [Delete Channel](actions/delete-channel.md) | DELETE | Deletes an existing channel from Recut URL Shortener. |
| [List Channels](actions/list-channels.md) | GET | Retrieves channels from Recut URL Shortener. |
| [Update Channel](actions/update-channel.md) | PUT | Updates an existing channel in Recut URL Shortener. |

### Cta Overlay

| Action | Method | Description |
| --- | --- | --- |
| [List CTA Overlays](actions/list-cta-overlays.md) | GET | Retrieves CTA overlays from Recut URL Shortener. |

### Custom Splash

| Action | Method | Description |
| --- | --- | --- |
| [List Custom Splash](actions/list-custom-splash.md) | GET | Retrieves custom splash pages from Recut URL Shortener. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [List Files](actions/list-files.md) | GET | Retrieves files from Recut URL Shortener. |
| [Upload File](actions/upload-file.md) | POST | Uploads a file to Recut URL Shortener. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [List Channel Items](actions/list-channel-items.md) | GET | Retrieves items from a channel in Recut URL Shortener. |

### Link

| Action | Method | Description |
| --- | --- | --- |
| [Delete Link](actions/delete-link.md) | DELETE | Deletes an existing link from Recut URL Shortener. |
| [Get Link](actions/get-link.md) | GET | Retrieves link details from Recut URL Shortener. |
| [List Links](actions/list-links.md) | GET | Retrieves links from Recut URL Shortener. |
| [Shorten Link](actions/shorten-link.md) | POST | Creates a shortened link in Recut URL Shortener. |
| [Update Link](actions/update-link.md) | PUT | Updates an existing link in Recut URL Shortener. |

### Pixel

| Action | Method | Description |
| --- | --- | --- |
| [Create Pixel](actions/create-pixel.md) | POST | Creates a tracking pixel in Recut URL Shortener. |
| [Delete Pixel](actions/delete-pixel.md) | DELETE | Deletes an existing tracking pixel from Recut URL Shortener. |
| [List Pixels](actions/list-pixels.md) | GET | Retrieves tracking pixels from Recut URL Shortener. |
| [Update Pixel](actions/update-pixel.md) | PUT | Updates an existing tracking pixel in Recut URL Shortener. |

### Qr Code

| Action | Method | Description |
| --- | --- | --- |
| [Create QR Code](actions/create-qr-code.md) | POST | Creates a QR code in Recut URL Shortener. |
| [Delete QR Code](actions/delete-qr-code.md) | DELETE | Deletes an existing QR code from Recut URL Shortener. |
| [Get QR Code](actions/get-qr-code.md) | GET | Retrieves QR code details from Recut URL Shortener. |
| [List QR Codes](actions/list-qr-codes.md) | GET | Retrieves QR codes from Recut URL Shortener. |
| [Update QR Code](actions/update-qr-code.md) | PUT | Updates an existing QR code in Recut URL Shortener. |

