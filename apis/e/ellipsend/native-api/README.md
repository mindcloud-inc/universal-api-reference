# Ellipsend: Native API Reference

A consolidated summary of Ellipsend's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://api.ellipsend.com/v1/docs
- **OpenAPI specification:** https://api.ellipsend.com/v1/swagger.yaml
- **API base URL:** `https://api.ellipsend.com/v1`

## Authentication

### OAuth2 (Client Credentials)

Generate Ellipsend client credentials and exchange them for API tokens.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://api.ellipsend.com/v1/auth/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `read write`.

A machine-to-machine flow is configured.

[Official authentication documentation](https://api.ellipsend.com/v1/docs)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Activity](actions/create-activity.md) | `POST https://api.ellipsend.com/v1/activity` | [docs](https://api.ellipsend.com/v1/docs#/Activity/post_v1_activity) |
| [Create Label](actions/create-label.md) | `POST /label` | [docs](https://api.ellipsend.com/v1/docs#/Label/post_label) |
| [Create Product](actions/create-product.md) | `POST /product` | [docs](https://api.ellipsend.com/v1/docs#/Product/post_v1_product) |
| [Create Status](actions/create-status.md) | `POST /status` | [docs](https://api.ellipsend.com/v1/docs#/Status/post_status) |
| [Delete Label](actions/delete-label.md) | `DELETE /label/[:label_id]` | [docs](https://api.ellipsend.com/v1/docs#/Label/delete_label__label_id_) |
| [Delete Status](actions/delete-status.md) | `DELETE /status/[:status_id]` | [docs](https://api.ellipsend.com/v1/docs#/Status/delete_status__status_id_) |
| [Get Activity](actions/get-activity.md) | `GET https://api.ellipsend.com/v1/activity/[:activity_id]` | [docs](https://api.ellipsend.com/v1/docs#/Activity/get_v1_activity__activity_id_) |
| [Get Activity Type](actions/get-activity-type.md) | `GET https://api.ellipsend.com/v1/activity-type/[:activity_type_id]` | [docs](https://api.ellipsend.com/v1/docs#/Activity%20Type/get_v1_activity_type__activity_type_id_) |
| [Get Assignee](actions/get-assignee.md) | `GET /assignee/[:assignee_id]` | [docs](https://api.ellipsend.com/v1/docs#/Assignee/get_assignee__assignee_id_) |
| [Get Company](actions/get-company.md) | `GET https://api.ellipsend.com/v1/company` | [docs](https://api.ellipsend.com/v1/docs#/Company/get_v1_company) |
| [Get Label](actions/get-label.md) | `GET /label/[:label_id]` | [docs](https://api.ellipsend.com/v1/docs#/Label/get_label__label_id_) |
| [Get Product](actions/get-product.md) | `GET /product/[:product_id]` | [docs](https://api.ellipsend.com/v1/docs#/Product/get_v1_product__product_id_) |
| [Get Status](actions/get-status.md) | `GET /status/[:status_id]` | [docs](https://api.ellipsend.com/v1/docs#/Status/get_status__status_id_) |
| [List Activity Types](actions/list-activity-types.md) | `GET https://api.ellipsend.com/v1/activity-type` | [docs](https://api.ellipsend.com/v1/docs#/Activity%20Type/get_v1_activity_type) |
| [List Assignees](actions/list-assignees.md) | `GET /assignee` | [docs](https://api.ellipsend.com/v1/docs#/Assignee/get_assignee) |
| [List Labels](actions/list-labels.md) | `GET /label` | [docs](https://api.ellipsend.com/v1/docs#/Label/get_label) |
| [List Products](actions/list-products.md) | `GET /product` | [docs](https://api.ellipsend.com/v1/docs#/Product/get_v1_product) |
| [List Statuses](actions/list-statuses.md) | `GET /status` | [docs](https://api.ellipsend.com/v1/docs#/Status/get_status) |
| [Update Contact](actions/update-contact.md) | `PUT /contact/[:token]` | [docs](https://api.ellipsend.com/v1/docs#/Contact/put_contact__token_) |
| [Update Label](actions/update-label.md) | `PUT /label/[:label_id]` | [docs](https://api.ellipsend.com/v1/docs#/Label/put_label__label_id_) |
| [Update Status](actions/update-status.md) | `PUT /status/[:status_id]` | [docs](https://api.ellipsend.com/v1/docs#/Status/put_status__status_id_) |
