# <img src="https://images.mindcloud.co/apps/icons/dubble_1775150291343.png" alt="Dubble logo" width="28" height="28"> Dubble: Universal API

Manage Dubble guides, collections, and webhooks

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dubble/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 16
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://dubble.so
- **Vendor API docs:** https://dubble.readme.io

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Collections](actions/list-collections.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dubble/latest/actions/list-collections?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (16)

### Collection

| Action | Method | Description |
| --- | --- | --- |
| [Create Collection](actions/create-collection.md) | POST | Creates a new collection in Dubble. |
| [Delete Collection](actions/delete-collection.md) | DELETE | Deletes an existing collection from Dubble. |
| [List Collections](actions/list-collections.md) | GET | Retrieves a list of collections from Dubble. |
| [Update Collection](actions/update-collection.md) | PUT | Updates an existing collection in Dubble. |

### Guide

| Action | Method | Description |
| --- | --- | --- |
| [Add Guide to Collection](actions/add-guide-to-collection.md) | PUT | Adds a guide to a collection in Dubble. |
| [Get Guide](actions/get-guide.md) | GET | Retrieves details for a guide from Dubble. |
| [List Guides](actions/list-guides.md) | GET | Retrieves a list of guides from Dubble. |
| [Remove Guide from Collection](actions/remove-guide-from-collection.md) | DELETE | Removes a guide from a collection in Dubble. |
| [Update Guide](actions/update-guide.md) | PUT | Updates an existing guide in Dubble. |

### Guidehtml

| Action | Method | Description |
| --- | --- | --- |
| [Get Guide as HTML](actions/get-guide-as-html.md) | GET | Retrieves a guide as HTML from Dubble. |

### Guidemarkdown

| Action | Method | Description |
| --- | --- | --- |
| [Get Guide as Markdown](actions/get-guide-as-markdown.md) | GET | Retrieves a guide as Markdown from Dubble. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Dubble. |
| [Create Webhook for Collection](actions/create-webhook-for-collection.md) | POST | Creates a new webhook for a collection in Dubble. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from Dubble. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves a list of webhooks from Dubble. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in Dubble. |

