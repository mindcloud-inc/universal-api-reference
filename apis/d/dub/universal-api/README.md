# <img src="https://images.mindcloud.co/apps/icons/dub_1774632757775.png" alt="Dub logo" width="28" height="28"> Dub: Universal API

Create short links and track partner conversions and analytics

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dub/latest
- **Category:** Marketing
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://dub.co
- **Vendor API docs:** https://dub.co/docs/api-reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Info](actions/get-user-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dub/latest/actions/get-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Domain

| Action | Method | Description |
| --- | --- | --- |
| [List Domains](actions/list-domains.md) | GET | Retrieves domains from Dub. |

### Domain Availability

| Action | Method | Description |
| --- | --- | --- |
| [Check Domain Availability](actions/check-domain-availability.md) | GET | Checks domain availability in Dub. |

### Link

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Create Links](actions/bulk-create-links.md) | POST | Creates links in Dub in bulk. |
| [Bulk Delete Links](actions/bulk-delete-links.md) | DELETE | Deletes links from Dub in bulk. |
| [Bulk Update Links](actions/bulk-update-links.md) | PUT | Updates links in Dub in bulk. |
| [Create Link](actions/create-link.md) | POST | Creates a link in Dub. |
| [Delete Link](actions/delete-link.md) | DELETE | Deletes a link from Dub. |
| [List Links](actions/list-links.md) | GET | Retrieves links from Dub. |
| [Retrieve Link](actions/retrieve-link.md) | GET | Retrieves a link from Dub. |
| [Update Link](actions/update-link.md) | PUT | Updates a link in Dub. |
| [Upsert Link](actions/upsert-link.md) | PUT | Updates or creates a link in Dub by URL. |

### Link Count

| Action | Method | Description |
| --- | --- | --- |
| [Count Links](actions/count-links.md) | GET | Retrieves the number of links in Dub. |

### Qr Code

| Action | Method | Description |
| --- | --- | --- |
| [Get QR Code](actions/get-qr-code.md) | GET | Retrieves a QR code for a Dub link. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a tag in Dub. |
| [Delete Tag](actions/delete-tag.md) | DELETE |  |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from Dub. |
| [Update Tag](actions/update-tag.md) | PUT | Updates a tag in Dub. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User Info](actions/get-user-info.md) | GET | Retrieves the authenticated user and workspace info from Dub. |

