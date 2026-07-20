# <img src="https://images.mindcloud.co/apps/icons/uniqode_1774557865870.png" alt="Uniqode logo" width="28" height="28"> Uniqode: Universal API

Uniqode is a QR code and engagement platform for managing dynamic and static QR codes, landing pages, forms, media, tags, webhooks, analytics, organizations, and related account assets through its REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/uniqode/latest
- **Category:** Marketing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.uniqode.com
- **Vendor API docs:** https://apidocs.uniqode.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Organizations](actions/list-organizations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uniqode/latest/actions/list-organizations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Landing Page

| Action | Method | Description |
| --- | --- | --- |
| [Create Landing Page](actions/create-landing-page.md) | POST | Creates a new landing page in Uniqode. |
| [Get Landing Page](actions/get-landing-page.md) | GET | Retrieves a landing page from your Uniqode account. |
| [List Landing Pages](actions/list-landing-pages.md) | GET | Retrieves landing pages from your Uniqode account. |
| [Update Landing Page](actions/update-landing-page.md) | PUT | Updates an existing landing page in Uniqode. |

### Media Object

| Action | Method | Description |
| --- | --- | --- |
| [Create Media Object](actions/create-media-object.md) | POST | Creates a new media object in Uniqode. |
| [Get Media Object](actions/get-media-object.md) | GET | Retrieves a media object from your Uniqode account. |
| [List Media Objects](actions/list-media-objects.md) | GET | Retrieves media objects from your Uniqode account. |
| [Update Media Object](actions/update-media-object.md) | PUT | Updates an existing media object in Uniqode. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization](actions/get-organization.md) | GET | Retrieves an organization from your Uniqode account. |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves organizations from your Uniqode account. |

### Qr Code

| Action | Method | Description |
| --- | --- | --- |
| [Activate QR Code](actions/activate-qr-code.md) | PUT | Activates a dynamic QR code in Uniqode. |
| [Create Dynamic QR Code (Custom URL)](actions/create-dynamic-qr-code-custom-url.md) | POST | Creates a dynamic custom URL QR code in Uniqode. |
| [Create Static QR Code (Website)](actions/create-static-qr-code-website.md) | POST | Creates a static website QR code in Uniqode. |
| [Deactivate QR Code](actions/deactivate-qr-code.md) | PUT | Deactivates a dynamic QR code in Uniqode. |
| [Delete QR Code](actions/delete-qr-code.md) | DELETE | Deletes an existing QR code from Uniqode. |
| [Download QR Code Image](actions/download-qr-code-image.md) | GET | Retrieves QR code image download URLs from Uniqode. |
| [Get QR Code](actions/get-qr-code.md) | GET | Retrieves a QR code from your Uniqode account. |
| [List QR Codes](actions/list-qr-codes.md) | GET | Retrieves QR codes from your Uniqode account. |
| [Update QR Code](actions/update-qr-code.md) | PUT | Updates an existing QR code in Uniqode. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a new tag in Uniqode. |
| [Delete Tag](actions/delete-tag.md) | DELETE | Deletes an existing tag from Uniqode. |
| [Get Tag](actions/get-tag.md) | GET | Retrieves a tag from your Uniqode account. |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from your Uniqode account. |
| [Update Tag](actions/update-tag.md) | PUT | Updates an existing tag in Uniqode. |

