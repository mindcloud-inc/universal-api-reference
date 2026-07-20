# <img src="https://images.mindcloud.co/apps/icons/klip-link_1775164892263.png" alt="KlipLink logo" width="28" height="28"> KlipLink: Universal API

KlipLink is a link management API for creating, updating, deleting, and listing short links and custom domains.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/klipLink/latest
- **Category:** Marketing
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://klipl.ink
- **Vendor API docs:** https://docs.klipl.ink/api/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Links](actions/list-links.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/klipLink/latest/actions/list-links?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Custom Objects

| Action | Method | Description |
| --- | --- | --- |
| [Create QR Code](actions/create-qr-code.md) | POST |  |
| [Delete Link](actions/delete-link.md) | DELETE |  |
| [Delete QR Code](actions/delete-qr-code.md) | DELETE |  |
| [Get QR Code](actions/get-qr-code.md) | GET |  |
| [List Domains](actions/list-domains.md) | GET |  |
| [List QR Codes](actions/list-qr-codes.md) | GET |  |
| [Update QR Code](actions/update-qr-code.md) | PUT |  |

### Link

| Action | Method | Description |
| --- | --- | --- |
| [Create Link](actions/create-link.md) | POST |  |
| [Get Link](actions/get-link.md) | GET |  |
| [List Links](actions/list-links.md) | GET |  |
| [Update Link](actions/update-link.md) | PUT |  |

