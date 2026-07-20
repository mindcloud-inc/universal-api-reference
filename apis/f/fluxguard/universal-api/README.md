# <img src="https://images.mindcloud.co/apps/icons/fluxguard-icon_1774893496429.png" alt="Fluxguard logo" width="28" height="28"> Fluxguard: Universal API

Monitor website changes and manage monitored pages and webhooks

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/fluxguard/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://fluxguard.com
- **Vendor API docs:** https://fluxguard.com/how-to-guides/use-our-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Data](actions/get-account-data.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fluxguard/latest/actions/get-account-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Data](actions/get-account-data.md) | GET | Retrieves your Fluxguard account attributes. |

### Category

| Action | Method | Description |
| --- | --- | --- |
| [Create Site Category](actions/create-site-category.md) | POST | Creates a new site category in Fluxguard. |
| [List Categories](actions/list-categories.md) | GET | Retrieves all categories from your Fluxguard account. |

### Crawl

| Action | Method | Description |
| --- | --- | --- |
| [Initiate Crawl](actions/initiate-crawl.md) | POST | Initiates a crawl for a Fluxguard monitoring session. |

### Page

| Action | Method | Description |
| --- | --- | --- |
| [Add Page](actions/add-page.md) | POST | Adds a new page for monitoring in Fluxguard. |
| [Delete Page](actions/delete-page.md) | DELETE | Deletes a monitored page from Fluxguard. |
| [Get Page Data](actions/get-page-data.md) | GET | Retrieves data for a monitored page from Fluxguard. |

### Site

| Action | Method | Description |
| --- | --- | --- |
| [Delete Site](actions/delete-site.md) | DELETE | Deletes a site and its monitoring data from Fluxguard. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Fluxguard. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes a webhook from Fluxguard. |
| [Get Sample Webhook](actions/get-sample-webhook.md) | GET | Retrieves a sample webhook payload from Fluxguard. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves your Fluxguard webhooks. |

