# Nyckel: Native API Reference

A consolidated summary of Nyckel's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://www.nyckel.com/docs
- **API base URL:** `https://www.nyckel.com/v1`

## Authentication

### OAuth 2.0

Use Nyckel OAuth2 client credentials to obtain bearer tokens for protected API requests.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://www.nyckel.com/connect/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


A machine-to-machine flow is configured.

[Official authentication documentation](https://www.nyckel.com/docs)

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Field](actions/create-field.md) | `POST /functions/:functionId/fields` |  |
| [Create Function](actions/create-function.md) | `POST /functions` |  |
| [Create Label](actions/create-label.md) | `POST /functions/:functionId/labels` | [docs](https://www.nyckel.com/docs#create-label) |
| [Create Text Sample](actions/create-text-sample.md) | `POST /functions/:functionId/samples` |  |
| [Delete Field](actions/delete-field.md) | `DELETE /functions/:functionId/fields/:fieldId` |  |
| [Delete Function](actions/delete-function.md) | `DELETE /functions/:functionId` |  |
| [Delete Label](actions/delete-label.md) | `DELETE /functions/:functionId/labels/:labelId` |  |
| [Delete Sample](actions/delete-sample.md) | `DELETE /functions/:functionId/samples/:sampleId` |  |
| [Delete Sample Annotation](actions/delete-sample-annotation.md) | `DELETE /functions/:functionId/samples/:sampleId/annotation` |  |
| [Get Field](actions/get-field.md) | `GET /functions/:functionId/fields/:fieldId` |  |
| [Get Function](actions/get-function.md) | `GET /functions/:functionId` |  |
| [Get Function Summary](actions/get-function-summary.md) | `GET /functions/:functionId/summary` | [docs](https://www.nyckel.com/docs) |
| [Get Label](actions/get-label.md) | `GET /functions/:functionId/labels/:labelId` |  |
| [Get Sample](actions/get-sample.md) | `GET /functions/:functionId/samples/:sampleId` |  |
| [List Fields](actions/list-fields.md) | `GET /functions/:functionId/fields` |  |
| [List Functions](actions/list-functions.md) | `GET /functions` | [docs](https://www.nyckel.com/docs) |
| [List Labels](actions/list-labels.md) | `GET /functions/:functionId/labels` |  |
| [List Samples](actions/list-samples.md) | `GET /functions/:functionId/samples` |  |
| [Set Sample Annotation](actions/set-sample-annotation.md) | `PUT /functions/:functionId/samples/:sampleId/annotation` |  |
| [Update Field](actions/update-field.md) | `PUT /functions/:functionId/fields/:fieldId` |  |
| [Update Label](actions/update-label.md) | `PUT /functions/:functionId/labels/:labelId` |  |
