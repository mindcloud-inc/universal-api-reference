# InventoryBase: Native API Reference

A consolidated summary of InventoryBase's API configuration and 41 documented operations, with links to official documentation.

- **Official docs:** https://developer.inventorybase.com/
- **API base URL:** `https://api.inventorybase.com`

## Authentication

### OAuth2

OAuth2 Authorization Code authentication for InventoryBase tenant accounts.

### Credentials

- **Client ID:** `clientId` · required · The OAuth client ID from your InventoryBase application. Create the application in the InventoryBase developer centre first.
- **Client Secret:** `clientSecret` · required · The OAuth client secret from your InventoryBase application in the developer centre.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://my.inventorybase.com/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://my.inventorybase.com/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `profile.read properties.read properties.write inspections.read inspections.write reports.read reports.write clients.read clients.write staff.read staff.write templates.read templates.write webhooks.read webhooks.write file-share.read file-share.write configuration.read configuration.write`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://my.inventorybase.com/oauth/token.

[Official authentication documentation](https://developer.inventorybase.com/#authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 30; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (41 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | `POST /clients` | [docs](https://developer.inventorybase.com/#create-a-client) |
| [Create Custom Field](actions/create-custom-field.md) | `POST /custom-fields` | [docs](https://developer.inventorybase.com/#create-a-custom-field) |
| [Create Inspection](actions/create-inspection.md) | `POST /inspections` | [docs](https://developer.inventorybase.com/#create-an-inspection) |
| [Create Inspection Contact](actions/create-inspection-contact.md) | `POST /inspections/:inspectionId/contacts` | [docs](https://developer.inventorybase.com/#create-an-inspection-contact) |
| [Create Property](actions/create-property.md) | `POST /properties` | [docs](https://developer.inventorybase.com/#creating-a-property) |
| [Create Property Contact](actions/create-property-contact.md) | `POST /properties/:propertyId/contacts` | [docs](https://developer.inventorybase.com/#create-a-property-contact) |
| [Create Property Meter](actions/create-property-meter.md) | `POST /properties/:propertyId/meters` | [docs](https://developer.inventorybase.com/#create-a-meter) |
| [Create Staff Member](actions/create-staff-member.md) | `POST /staff` | [docs](https://developer.inventorybase.com/#create-a-staff-member) |
| [Delete Custom Field](actions/delete-custom-field.md) | `DELETE /custom-fields/:customFieldId` | [docs](https://developer.inventorybase.com/#delete-a-custom-field) |
| [Delete Inspection Contact](actions/delete-inspection-contact.md) | `DELETE /inspections/:inspectionId/contacts/:contactId` | [docs](https://developer.inventorybase.com/#delete-an-inspection-contact) |
| [Delete Property Contact](actions/delete-property-contact.md) | `DELETE /properties/:propertyId/contacts/:contactId` | [docs](https://developer.inventorybase.com/#delete-a-property-contact) |
| [Delete Property Meter](actions/delete-property-meter.md) | `DELETE /properties/:propertyId/meters/:meterId` | [docs](https://developer.inventorybase.com/#delete-a-meter) |
| [Delete Webhook Listener](actions/delete-webhook-listener.md) | `DELETE /webhooks/:webhookId` | [docs](https://developer.inventorybase.com/#delete-a-webhook-listener) |
| [Get Client](actions/get-client.md) | `GET /clients/:clientId` | [docs](https://developer.inventorybase.com/#get-a-single-client) |
| [Get Current User](actions/get-current-user.md) | `GET /me` | [docs](https://developer.inventorybase.com/#making-authenticated-api-requests) |
| [Get Inspection](actions/get-inspection.md) | `GET /inspections/:inspectionId` | [docs](https://developer.inventorybase.com/#get-an-inspection) |
| [Get Inspection Report](actions/get-inspection-report.md) | `GET /inspections/:inspectionId/report` | [docs](https://developer.inventorybase.com/#retrieve-inspection-report) |
| [Get Inspection Report Metadata](actions/get-inspection-report-metadata.md) | `GET /inspections/:inspectionId/report/metadata` | [docs](https://developer.inventorybase.com/#retrieve-inspection-metadata-meters-alarms-keys-manuals) |
| [Get Property](actions/get-property.md) | `GET /properties/:propertyId` | [docs](https://developer.inventorybase.com/#get-a-single-property) |
| [Get Property Meter](actions/get-property-meter.md) | `GET /properties/:propertyId/meters/:meterId` | [docs](https://developer.inventorybase.com/#get-a-single-meter) |
| [Get Staff Member](actions/get-staff-member.md) | `GET /staff/:staffId` | [docs](https://developer.inventorybase.com/#get-a-single-staff-member) |
| [Get Template Report](actions/get-template-report.md) | `GET /templates/:templateId/report` | [docs](https://developer.inventorybase.com/#retrieve-inspection-report) |
| [List Action Reports by Inspection](actions/list-action-reports-by-inspection.md) | `GET /inspections/:inspectionId/action-reports` | [docs](https://developer.inventorybase.com/#list-action-reports-by-inspection) |
| [List Clients](actions/list-clients.md) | `GET /clients` | [docs](https://developer.inventorybase.com/#list-all-clients) |
| [List Custom Fields](actions/list-custom-fields.md) | `GET /custom-fields` | [docs](https://developer.inventorybase.com/#list-all-custom-fields) |
| [List Inspection Contacts](actions/list-inspection-contacts.md) | `GET /inspections/:inspectionId/contacts` | [docs](https://developer.inventorybase.com/#list-contacts-for-an-inspection) |
| [List Inspections](actions/list-inspections.md) | `GET /inspections` | [docs](https://developer.inventorybase.com/#list-all-inspections) |
| [List Properties](actions/list-properties.md) | `GET /properties` | [docs](https://developer.inventorybase.com/#list-all-properties) |
| [List Property Contacts](actions/list-property-contacts.md) | `GET /properties/:propertyId/contacts` | [docs](https://developer.inventorybase.com/#list-contacts-for-a-property) |
| [List Property Meters](actions/list-property-meters.md) | `GET /properties/:propertyId/meters` | [docs](https://developer.inventorybase.com/#list-all-meters) |
| [List Staff Members](actions/list-staff-members.md) | `GET /staff` | [docs](https://developer.inventorybase.com/#list-all-staff) |
| [Load Template into Inspection](actions/load-template-into-inspection.md) | `PUT /inspections/:inspectionId/templates/:templateId` | [docs](https://developer.inventorybase.com/#loading-an-template) |
| [Register Webhook Listener](actions/register-webhook-listener.md) | `POST /webhooks` | [docs](https://developer.inventorybase.com/#register-a-webhooks-listener) |
| [Update Client](actions/update-client.md) | `PUT /clients/:clientId` | [docs](https://developer.inventorybase.com/#update-a-client) |
| [Update Custom Field](actions/update-custom-field.md) | `PUT /custom-fields/:customFieldId` | [docs](https://developer.inventorybase.com/#update-a-custom-field) |
| [Update Inspection](actions/update-inspection.md) | `PUT /inspections/:inspectionId` | [docs](https://developer.inventorybase.com/#update-an-inspection) |
| [Update Inspection Contact](actions/update-inspection-contact.md) | `PUT /inspections/:inspectionId/contacts/:contactId` | [docs](https://developer.inventorybase.com/#update-an-inspection-contact) |
| [Update Property](actions/update-property.md) | `PUT /properties/:propertyId` | [docs](https://developer.inventorybase.com/#update-a-property) |
| [Update Property Contact](actions/update-property-contact.md) | `PUT /properties/:propertyId/contacts/:contactId` | [docs](https://developer.inventorybase.com/#update-a-property-contact) |
| [Update Property Meter](actions/update-property-meter.md) | `PUT /properties/:propertyId/meters/:meterId` | [docs](https://developer.inventorybase.com/#update-a-meter) |
| [Update Staff Member](actions/update-staff-member.md) | `PUT /staff/:staffId` | [docs](https://developer.inventorybase.com/#update-a-staff-member) |
