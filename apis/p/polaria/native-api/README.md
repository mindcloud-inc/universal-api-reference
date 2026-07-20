# Polaria: Native API Reference

A consolidated summary of Polaria's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://help.polaria.ai/hc/rest-api?lang=en
- **API base URL:** `https://app.polaria.ai/rest/v2`

## Authentication

### OAuth 2

Connect Polaria using OAuth 2.0.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://app.polaria.ai/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://app.polaria.ai/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `widgets faqs contacts conversations`.

[Official authentication documentation](https://help.polaria.ai/hc/rest-api-authentication/oauth-2-2?lang=en)

### API Key

Connect Polaria with a chatbox Secret Key. MindCloud will send the secret key as a Bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.polaria.ai/hc/rest-api-authentication/find-my-chatbox-secret-key?lang=en)

## API conventions

The next-page cursor is read from `next_page`. The total page count is read from `total_pages`.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Brand](actions/create-brand.md) | `POST /widgets` | [docs](https://help.polaria.ai/hc/rest-api-brands/post-widgets-create-a-brand?lang=en) |
| [Create Post](actions/create-post.md) | `POST /faqs` | [docs](https://help.polaria.ai/hc/rest-api-posts/post-faqs-create-a-post?lang=en) |
| [Create Post Category](actions/create-post-category.md) | `POST /faq_categories` | [docs](https://help.polaria.ai/hc/rest-api-post-categories/post-faq_categories-create-a-post-category?lang=en) |
| [Create Webhook](actions/create-webhook.md) | `POST /widgets/[:api_key]/webhooks` | [docs](https://help.polaria.ai/hc/rest-api-webhooks/post-widgets-api_key-webhooks-id-create-a-webhook-2?lang=en) |
| [Delete Brand](actions/delete-brand.md) | `DELETE /widgets/[:api_key]` | [docs](https://help.polaria.ai/hc/rest-api-brands/del-widgets-api_key-delete-a-brand?lang=en) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /widgets/[:api_key]/contacts/[:id]` | [docs](https://help.polaria.ai/hc/rest-api-contacts/del-widgets-api_key-contacts-id-delete-a-contact?lang=en) |
| [Delete Post](actions/delete-post.md) | `DELETE /faqs/[:id]` | [docs](https://help.polaria.ai/hc/rest-api-posts/del-faqs-id-delete-a-post?lang=en) |
| [Delete Post Category](actions/delete-post-category.md) | `DELETE /faq_categories/[:id]` | [docs](https://help.polaria.ai/hc/rest-api-post-categories/del-faq_categories-id-delete-a-post?lang=en) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /widgets/[:api_key]/webhooks/[:id]` | [docs](https://help.polaria.ai/hc/rest-api-webhooks/del-widgets-api_key-webhooks-id-delete-a-webhook-2?lang=en) |
| [List Brands](actions/list-brands.md) | `GET /widgets` | [docs](https://help.polaria.ai/hc/rest-api-brands/get-widgets-list-brands?lang=en) |
| [List Contacts](actions/list-contacts.md) | `GET /widgets/[:api_key]/contacts` | [docs](https://help.polaria.ai/hc/rest-api-contacts/get-widgets-api_key-contacts-list-contacts?lang=en) |
| [List Post Categories](actions/list-post-categories.md) | `GET /faq_categories` | [docs](https://help.polaria.ai/hc/rest-api-post-categories/get-faq_categories-list-post-categories?lang=en) |
| [List Posts](actions/list-posts.md) | `GET /faqs` | [docs](https://help.polaria.ai/hc/rest-api-posts/get-faqs-list-posts?lang=en) |
| [List Webhooks](actions/list-webhooks.md) | `GET /widgets/[:api_key]/webhooks` | [docs](https://help.polaria.ai/hc/rest-api-webhooks/get-widgets-api_key-webhooks-list-webhooks-2?lang=en) |
| [Retrieve Brand](actions/retrieve-brand.md) | `GET /widgets/[:api_key]` | [docs](https://help.polaria.ai/hc/rest-api-brands/get-widgets-api_key-retrieve-a-brand?lang=en) |
| [Retrieve Contact](actions/retrieve-contact.md) | `GET /widgets/[:api_key]/contacts/[:id]` | [docs](https://help.polaria.ai/hc/rest-api-contacts/get-widgets-api_key-contacts-id-retrieve-a-contact?lang=en) |
| [Retrieve Contact by Cookie Token](actions/retrieve-contact-by-cookie-token.md) | `GET /widgets/[:api_key]/contacts/retrieve` | [docs](https://help.polaria.ai/hc/rest-api-contacts/get-widgets-api_key-contacts-retrieve-retrieve-a-contact-by-cookie_token?lang=en) |
| [Retrieve Post](actions/retrieve-post.md) | `GET /faqs/[:id]` | [docs](https://help.polaria.ai/hc/rest-api-posts/get-faqs-id-retrieve-a-post?lang=en) |
| [Retrieve Post Category](actions/retrieve-post-category.md) | `GET /faq_categories/[:id]` | [docs](https://help.polaria.ai/hc/rest-api-post-categories/get-faq_categories-id-retrieve-a-post-category?lang=en) |
| [Retrieve Webhook](actions/retrieve-webhook.md) | `GET /widgets/[:api_key]/webhooks/[:id]` | [docs](https://help.polaria.ai/hc/rest-api-webhooks/get-widgets-api_key-webhooks-id-retrieve-a-webhook-2?lang=en) |
| [Update Brand](actions/update-brand.md) | `PUT /widgets/[:api_key]` | [docs](https://help.polaria.ai/hc/rest-api-brands/put-widgets-api_key-update-a-brand?lang=en) |
| [Update Contact](actions/update-contact.md) | `PUT /widgets/[:api_key]/contacts/[:id]` | [docs](https://help.polaria.ai/hc/rest-api-contacts/put-widgets-api_key-contacts-id-update-a-contact?lang=en) |
| [Update Post](actions/update-post.md) | `PUT /faqs/[:id]` | [docs](https://help.polaria.ai/hc/rest-api-posts/put-faqs-id-update-a-post?lang=en) |
| [Update Post Category](actions/update-post-category.md) | `PUT /faq_categories/[:id]` | [docs](https://help.polaria.ai/hc/rest-api-post-categories/put-faq_categories-id-update-a-post-category?lang=en) |
