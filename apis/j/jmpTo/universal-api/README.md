# <img src="https://images.mindcloud.co/apps/icons/jmp-to_1776201299212.png" alt="JmpTo logo" width="28" height="28"> JmpTo: Universal API

Create, organize, and track short links, campaigns, channels, pixels, branded domains, and QR codes in JmpTo.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/jmpTo/latest
- **Category:** Marketing
- **Actions:** 29
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://jmpto.net
- **Vendor API docs:** https://jmpto.net/developers

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (29)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves account details from JmpTo. |

### Branded Domain

| Action | Method | Description |
| --- | --- | --- |
| [List Branded Domains](actions/list-branded-domains.md) | GET | Retrieves branded domains from JmpTo. |

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Assign Link to Campaign](actions/assign-link-to-campaign.md) | PUT | Assigns a link to a campaign in JmpTo. |
| [Create Campaign](actions/create-campaign.md) | POST | Creates a campaign in JmpTo. |
| [Delete Campaign](actions/delete-campaign.md) | DELETE | Deletes an existing campaign from JmpTo. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaigns from JmpTo. |
| [Update Campaign](actions/update-campaign.md) | PUT | Updates an existing campaign in JmpTo. |

### Channel Item

| Action | Method | Description |
| --- | --- | --- |
| [List Channel Items](actions/list-channel-items.md) | GET | Retrieves items from a channel in JmpTo. |

### Channels

| Action | Method | Description |
| --- | --- | --- |
| [Assign Item to Channel](actions/assign-item-to-channel.md) | PUT | Assigns an item to a channel in JmpTo. |
| [Create Channel](actions/create-channel.md) | POST | Creates a channel in JmpTo. |
| [Delete Channel](actions/delete-channel.md) | DELETE | Deletes an existing channel from JmpTo. |
| [List Channels](actions/list-channels.md) | GET | Retrieves channels from JmpTo. |
| [Update Channel](actions/update-channel.md) | PUT | Updates an existing channel in JmpTo. |

### Cta Overlay

| Action | Method | Description |
| --- | --- | --- |
| [List CTA Overlays](actions/list-cta-overlays.md) | GET | Retrieves CTA overlays from JmpTo. |

### Custom Splash Page

| Action | Method | Description |
| --- | --- | --- |
| [List Custom Splash Pages](actions/list-custom-splash-pages.md) | GET | Retrieves custom splash pages from JmpTo. |

### Link

| Action | Method | Description |
| --- | --- | --- |
| [Delete Link](actions/delete-link.md) | DELETE | Deletes an existing link from JmpTo. |
| [Get Link](actions/get-link.md) | GET | Retrieves a link from JmpTo. |
| [List Links](actions/list-links.md) | GET | Retrieves links from JmpTo. |
| [Shorten Link](actions/shorten-link.md) | POST | Creates a shortened link in JmpTo. |
| [Update Link](actions/update-link.md) | PUT | Updates an existing link in JmpTo. |

### Pixel

| Action | Method | Description |
| --- | --- | --- |
| [Create Pixel](actions/create-pixel.md) | POST | Creates a pixel in JmpTo. |
| [Delete Pixel](actions/delete-pixel.md) | DELETE | Deletes an existing pixel from JmpTo. |
| [List Pixels](actions/list-pixels.md) | GET | Retrieves pixels from JmpTo. |
| [Update Pixel](actions/update-pixel.md) | PUT | Updates an existing pixel in JmpTo. |

### Qr Code

| Action | Method | Description |
| --- | --- | --- |
| [Create QR Code](actions/create-qr-code.md) | POST | Creates a QR code in JmpTo. |
| [Delete QR Code](actions/delete-qr-code.md) | DELETE | Deletes an existing QR code from JmpTo. |
| [Get QR Code](actions/get-qr-code.md) | GET | Retrieves a QR code from JmpTo. |
| [List QR Codes](actions/list-qr-codes.md) | GET | Retrieves QR codes from JmpTo. |
| [Update QR Code](actions/update-qr-code.md) | PUT | Updates an existing QR code in JmpTo. |

