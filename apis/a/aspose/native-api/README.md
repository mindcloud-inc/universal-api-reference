# Aspose: Native API Reference

A consolidated summary of Aspose's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.aspose.cloud/slides/
- **API base URL:** `https://api.aspose.cloud/v3.0`

## Authentication

### OAuth 2.0

Use Aspose Cloud OAuth2 client credentials to obtain a bearer token for protected API requests.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://api.aspose.cloud/connect/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


A machine-to-machine flow is configured.

[Official authentication documentation](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Custom Properties](actions/add-custom-properties.md) | `POST /slides/:name/documentproperties` | [docs](https://docs.aspose.cloud/slides/add-custom-properties/) |
| [Copy Slide](actions/copy-slide.md) | `POST /slides/:name/slides/copy` | [docs](https://docs.aspose.cloud/slides/copy-slides/) |
| [Create Presentation](actions/create-presentation.md) | `POST /slides/:name` | [docs](https://docs.aspose.cloud/slides/create-a-new-presentation/) |
| [Create Shape](actions/create-shape.md) | `POST /slides/:name/slides/:slideIndex/shapes` | [docs](https://docs.aspose.cloud/slides/add-a-shape-to-a-slide/) |
| [Create Slide](actions/create-slide.md) | `POST /slides/:name/slides` | [docs](https://docs.aspose.cloud/slides/add-a-new-slide/) |
| [Delete Document Property](actions/delete-document-property.md) | `DELETE /slides/:name/documentproperties/:propertyName` | [docs](https://docs.aspose.cloud/slides/delete-document-properties/) |
| [Delete Shape](actions/delete-shape.md) | `DELETE /slides/:name/slides/:slideIndex/shapes/:shapeIndex` | [docs](https://docs.aspose.cloud/slides/delete-shapes-from-a-slide/) |
| [Delete Slide](actions/delete-slide.md) | `DELETE /slides/:name/slides/:slideIndex` | [docs](https://docs.aspose.cloud/slides/delete-slides/) |
| [Delete Slides](actions/delete-slides.md) | `DELETE /slides/:name/slides` | [docs](https://docs.aspose.cloud/slides/delete-slides/) |
| [Get API Information](actions/get-api-information.md) | `GET /slides/info` | [docs](https://docs.aspose.cloud/slides/get-api-information/) |
| [Get Document Property](actions/get-document-property.md) | `GET /slides/:name/documentproperties/:propertyName` | [docs](https://docs.aspose.cloud/slides/read-document-properties/) |
| [Get Presentation](actions/get-presentation.md) | `GET /slides/:name` | [docs](https://docs.aspose.cloud/slides/read-information-about-a-presentation/) |
| [Get Shape](actions/get-shape.md) | `GET /slides/:name/slides/:slideIndex/shapes/:shapeIndex` | [docs](https://docs.aspose.cloud/slides/get-a-shape-from-a-slide/) |
| [Get Slide](actions/get-slide.md) | `GET /slides/:name/slides/:slideIndex` | [docs](https://docs.aspose.cloud/slides/get-information-about-slides/) |
| [List Document Properties](actions/list-document-properties.md) | `GET /slides/:name/documentproperties` | [docs](https://docs.aspose.cloud/slides/read-document-properties/) |
| [List Presentation Text Items](actions/list-presentation-text-items.md) | `GET /slides/:name/textItems` | [docs](https://docs.aspose.cloud/slides/read-text-items/) |
| [List Shapes](actions/list-shapes.md) | `GET /slides/:name/slides/:slideIndex/shapes` | [docs](https://docs.aspose.cloud/slides/get-shapes-from-a-slide/) |
| [List Slide Placeholders](actions/list-slide-placeholders.md) | `GET /slides/:name/slides/:slideIndex/placeholders` | [docs](https://docs.aspose.cloud/slides/get-placeholders-from-a-slide/) |
| [List Slide Text Items](actions/list-slide-text-items.md) | `GET /slides/:name/slides/:slideIndex/textItems` | [docs](https://docs.aspose.cloud/slides/read-text-items/) |
| [List Slides](actions/list-slides.md) | `GET /slides/:name/slides` | [docs](https://docs.aspose.cloud/slides/get-information-about-slides/) |
| [Move Slide](actions/move-slide.md) | `POST /slides/:name/slides/:slideIndex/move` | [docs](https://docs.aspose.cloud/slides/move-a-slide/) |
| [Replace Presentation Text](actions/replace-presentation-text.md) | `POST /slides/:name/replaceText` | [docs](https://docs.aspose.cloud/slides/replace-a-text-occurrence/) |
| [Replace Slide Text](actions/replace-slide-text.md) | `POST /slides/:name/slides/:slideIndex/replaceText` | [docs](https://docs.aspose.cloud/slides/replace-a-text-occurrence/) |
| [Update Document Property](actions/update-document-property.md) | `PUT /slides/:name/documentproperties/:propertyName` | [docs](https://docs.aspose.cloud/slides/update-document-properties/) |
