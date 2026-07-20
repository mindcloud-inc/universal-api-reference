# <img src="https://images.mindcloud.co/apps/icons/hyperise_1775059899239.png" alt="Hyperise logo" width="28" height="28"> Hyperise: Universal API

Create personalized images, short links, prospect data, and view tracking

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/hyperise/latest
- **Category:** Marketing
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://hyperise.io
- **Vendor API docs:** https://hyperise.customerly.help/en/collections/4317-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hyperise/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### Business

| Action | Method | Description |
| --- | --- | --- |
| [Create Business](actions/create-business.md) | POST | Creates a new business in Hyperise. |
| [Delete Business](actions/delete-business.md) | DELETE | Deletes an existing business from Hyperise. |
| [Get Business](actions/get-business.md) | GET | Retrieves a business from Hyperise. |
| [List Businesses](actions/list-businesses.md) | GET | Retrieves businesses from Hyperise. |
| [Update Business](actions/update-business.md) | PUT | Updates an existing business in Hyperise. |

### Enriched Prospect

| Action | Method | Description |
| --- | --- | --- |
| [Get Enriched Prospect Data](actions/get-enriched-prospect-data.md) | GET | Retrieves enriched prospect data from Hyperise by email address. |

### Image Template

| Action | Method | Description |
| --- | --- | --- |
| [List Image Templates](actions/list-image-templates.md) | GET | Retrieves image templates from Hyperise. |

### Image View

| Action | Method | Description |
| --- | --- | --- |
| [List Image Views](actions/list-image-views.md) | GET | Retrieves image views for an image template in Hyperise. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Create Organization](actions/create-organization.md) | POST | Creates a client organization in Hyperise. |

### Short Link

| Action | Method | Description |
| --- | --- | --- |
| [Create Short Link](actions/create-short-link.md) | POST | Creates a personalized short link in Hyperise. |
| [List Short Links](actions/list-short-links.md) | GET | Retrieves short links from Hyperise. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Hyperise. |

