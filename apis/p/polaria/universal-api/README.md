# <img src="https://images.mindcloud.co/apps/icons/polaria_1775600371102.jpeg" alt="Polaria logo" width="28" height="28"> Polaria: Universal API

Manage Polaria brands, contacts, posts, categories, and webhooks

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/polaria/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://polaria.ai
- **Vendor API docs:** https://help.polaria.ai/hc/rest-api?lang=en

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Brands](actions/list-brands.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/polaria/latest/actions/list-brands?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Brand

| Action | Method | Description |
| --- | --- | --- |
| [Create Brand](actions/create-brand.md) | POST | Creates a new brand in Polaria. |
| [Delete Brand](actions/delete-brand.md) | DELETE | Deletes a brand from Polaria. |
| [List Brands](actions/list-brands.md) | GET | Retrieves brands from Polaria. |
| [Retrieve Brand](actions/retrieve-brand.md) | GET | Retrieves a brand from Polaria by API key. |
| [Update Brand](actions/update-brand.md) | PUT | Updates an existing brand in Polaria. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes a contact from Polaria. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from a Polaria brand. |
| [Retrieve Contact](actions/retrieve-contact.md) | GET | Retrieves a contact from Polaria. |
| [Retrieve Contact by Cookie Token](actions/retrieve-contact-by-cookie-token.md) | GET | Retrieves a contact from Polaria by cookie token. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Polaria. |

### Post

| Action | Method | Description |
| --- | --- | --- |
| [Create Post](actions/create-post.md) | POST | Creates a new post in Polaria. |
| [Delete Post](actions/delete-post.md) | DELETE | Deletes a post from Polaria. |
| [List Posts](actions/list-posts.md) | GET | Retrieves posts from Polaria. |
| [Retrieve Post](actions/retrieve-post.md) | GET | Retrieves a post from Polaria. |
| [Update Post](actions/update-post.md) | PUT | Updates an existing post in Polaria. |

### Post Category

| Action | Method | Description |
| --- | --- | --- |
| [Create Post Category](actions/create-post-category.md) | POST | Creates a new post category in Polaria. |
| [Delete Post Category](actions/delete-post-category.md) | DELETE | Deletes a post category from Polaria. |
| [List Post Categories](actions/list-post-categories.md) | GET | Retrieves post categories from Polaria. |
| [Retrieve Post Category](actions/retrieve-post-category.md) | GET | Retrieves a post category from Polaria. |
| [Update Post Category](actions/update-post-category.md) | PUT | Updates an existing post category in Polaria. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Polaria. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes a webhook from Polaria. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from a Polaria brand. |
| [Retrieve Webhook](actions/retrieve-webhook.md) | GET | Retrieves a webhook from Polaria. |

