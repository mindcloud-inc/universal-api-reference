# Trust: Native API Reference

A consolidated summary of Trust's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://api-docs.usetrust.io
- **OpenAPI specification:** https://api.usetrust.app/swagger/v1/swagger.json
- **API base URL:** `https://api.usetrust.app/v1`

## Authentication

### Basic

Use Trust basic auth with username `dummy` and the Trust API key as the password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://api-docs.usetrust.io/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Assign Testimonial To Widget](actions/assign-testimonial-to-widget.md) | `PUT /testimonial/:id/assign-widget/:widgetId` | [docs](https://api-docs.usetrust.io/api-reference-swagger) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://api-docs.usetrust.io/api-reference-swagger) |
| [Create Testimonial](actions/create-testimonial.md) | `POST /testimonial` | [docs](https://api-docs.usetrust.io/api-reference-swagger) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contacts/:id` | [docs](https://api-docs.usetrust.io/api-reference-swagger) |
| [Delete Testimonial](actions/delete-testimonial.md) | `DELETE /testimonial/:id` | [docs](https://api-docs.usetrust.io/api-reference-swagger) |
| [Find Contact By Email](actions/find-contact-by-email.md) | `GET /contacts` | [docs](https://api-docs.usetrust.io/api-reference-swagger) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:id` | [docs](https://api-docs.usetrust.io/api-reference-swagger) |
| [Get Testimonial](actions/get-testimonial.md) | `GET /testimonial/:id` | [docs](https://api-docs.usetrust.io/api-reference-swagger) |
| [List Campaigns](actions/list-campaigns.md) | `GET /campaigns/all/:workspaceId` | [docs](https://api-docs.usetrust.io/api-reference-swagger) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts/all/:workspaceId` | [docs](https://api-docs.usetrust.io/api-reference-swagger) |
| [List Testimonials](actions/list-testimonials.md) | `GET /testimonial/all/:workspaceId` | [docs](https://api-docs.usetrust.io/api-reference-swagger) |
| [List Widgets](actions/list-widgets.md) | `GET /widgets` | [docs](https://api-docs.usetrust.io/api-reference-swagger) |
| [List Workspaces](actions/list-workspaces.md) | `GET /workspaces` | [docs](https://api-docs.usetrust.io/api-reference-swagger) |
| [Remove Testimonial From Widget](actions/remove-testimonial-from-widget.md) | `PUT /testimonial/:id/remove-widget/:widgetId` | [docs](https://api-docs.usetrust.io/api-reference-swagger) |
| [Update Contact](actions/update-contact.md) | `PUT /contacts/:id` | [docs](https://api-docs.usetrust.io/api-reference-swagger) |
| [Update Testimonial](actions/update-testimonial.md) | `PUT /testimonial/:id` | [docs](https://api-docs.usetrust.io/api-reference-swagger) |
| [Upload Contact Image](actions/upload-contact-image.md) | `POST /contacts/upload-image/:workspaceId` | [docs](https://api-docs.usetrust.io/api-reference-swagger) |
| [Upload Media Image](actions/upload-media-image.md) | `POST /media/upload-image/:workspaceId` | [docs](https://api-docs.usetrust.io/api-reference-swagger) |
| [Upload Small Video](actions/upload-small-video.md) | `POST /media/upload-small-video/:workspaceId` | [docs](https://api-docs.usetrust.io/api-reference-swagger) |
| [Upload Video](actions/upload-video.md) | `POST /media/upload-video/:workspaceId` | [docs](https://api-docs.usetrust.io/api-reference-swagger) |
