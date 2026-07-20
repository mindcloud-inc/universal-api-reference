# <img src="https://images.mindcloud.co/apps/icons/logo-linktwin-2_1775841525876.png" alt="LinkTwin logo" width="28" height="28"> LinkTwin: Universal API

Create, manage, and track deep links, short URLs, and analytics

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/linkTwin/latest
- **Category:** Marketing
- **Actions:** 29
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://linktw.in
- **Vendor API docs:** https://linktw.in/developers

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (29)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves your account details from LinkTwin. |

### Collection

| Action | Method | Description |
| --- | --- | --- |
| [Assign Link To Collection](actions/assign-link-to-collection.md) | PUT | Assigns a link to a collection in LinkTwin. |
| [Bulk Assign Links To Collection](actions/bulk-assign-links-to-collection.md) | PUT | Adds or removes multiple links for a collection in LinkTwin. |
| [Create Collection](actions/create-collection.md) | POST | Creates a new collection in LinkTwin. |
| [Delete Collection](actions/delete-collection.md) | DELETE | Deletes an existing collection from LinkTwin and unassigns its items. |
| [Get Collection](actions/get-collection.md) | GET | Retrieves a collection and its items from LinkTwin. |
| [List Collections](actions/list-collections.md) | GET | Retrieves your saved collections from LinkTwin. |
| [Update Collection](actions/update-collection.md) | PUT | Updates an existing collection in LinkTwin. |

### Link

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Delete Links](actions/bulk-delete-links.md) | DELETE | Deletes multiple existing links from LinkTwin. |
| [Create Link](actions/create-link.md) | POST | Creates a new shortened link in LinkTwin. |
| [Delete Link](actions/delete-link.md) | DELETE | Deletes an existing link from LinkTwin. |
| [Get Link](actions/get-link.md) | GET | Retrieves a link from LinkTwin by ID or short URL. |
| [List Links](actions/list-links.md) | GET | Retrieves your shortened links from LinkTwin. |
| [Update Link](actions/update-link.md) | PUT | Updates an existing link in LinkTwin. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Assign Links To Pixel](actions/bulk-assign-links-to-pixel.md) | PUT | Adds or removes multiple links for a pixel in LinkTwin. |
| [Create Branded Domain](actions/create-branded-domain.md) | POST | Creates a new branded domain in LinkTwin. |
| [Create Pixel](actions/create-pixel.md) | POST | Creates a new tracking pixel in LinkTwin. |
| [Create QR Code](actions/create-qr-code.md) | POST | Creates a new QR code in LinkTwin. |
| [Delete Domain](actions/delete-domain.md) | DELETE | Deletes an existing branded domain from LinkTwin. |
| [Delete Pixel](actions/delete-pixel.md) | DELETE | Deletes an existing pixel from LinkTwin. |
| [Delete QR Code](actions/delete-qr-code.md) | DELETE | Deletes an existing QR code from LinkTwin. |
| [Get Pixel](actions/get-pixel.md) | GET | Retrieves a pixel and its assigned links from LinkTwin. |
| [Get QR Code](actions/get-qr-code.md) | GET | Retrieves a QR code from LinkTwin. |
| [List Domains](actions/list-domains.md) | GET | Retrieves standard and branded domains from LinkTwin. |
| [List Pixels](actions/list-pixels.md) | GET | Retrieves your tracking pixels from LinkTwin. |
| [List QR Codes](actions/list-qr-codes.md) | GET | Retrieves your QR codes from LinkTwin. |
| [Update Domain](actions/update-domain.md) | PUT | Updates an existing branded domain in LinkTwin. |
| [Update Pixel](actions/update-pixel.md) | PUT | Updates an existing pixel in LinkTwin. |
| [Update QR Code](actions/update-qr-code.md) | PUT | Updates an existing QR code in LinkTwin. |

