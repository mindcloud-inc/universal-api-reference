# 3E Protect: Native API Reference

A consolidated summary of 3E Protect's API configuration and 37 documented operations, with links to official documentation.

- **Official docs:** https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/index.html
- **OpenAPI specification:** https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json
- **REST API base URL:** `{apiBaseUrl}`
- **REST API base URL:** `{documentSearchApiBaseUrl}`

## Authentication

### OAuth 2.0

Choose Production or QC/Beta and enter the matching Client ID and Client Secret supplied by your 3E Implementation Manager.

### Credentials

- **Environment:** `environment` · required · Choose Production for live access or QC/Beta for testing. Use credentials issued for the selected environment.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to {{credentials.tokenUrl}}.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `account-services.account-specific`.

A machine-to-machine flow is configured.

[Official authentication documentation](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/index.html)

## API conventions

### REST API

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

### REST API

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The current page number is read from `pageNumber`.

## Pagination

- **REST API:** Use `page` in the request parameters to choose the page; numbering starts at 1.
- **REST API:** Use `pageSize` in the request body to set the page size (default 100; minimum 1). Use `pageNumber` in the request body to choose the page; numbering starts at 1.

## Endpoints (37 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Catalog Item Identifiers](actions/add-catalog-item-identifiers.md) | `PUT /catalog-item/productidentifier/:source/:identifier` | [docs](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1catalog-item~1productidentifier~1{source}~1{identifier}/put) |
| [Add Location SDS Requirement](actions/add-location-sds-requirement.md) | `POST /location-obtainment` | [docs](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1location-obtainment/post) |
| [Assign Catalog Item to Location](actions/assign-catalog-item-to-location.md) | `PUT /inventory-assignment/:source/:identifier/:targetLocationGuid` | [docs](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1inventory-assignment~1{source}~1{identifier}~1{targetLocationGuid}/put) |
| [Assign Catalog Item to Location by GUID](actions/assign-catalog-item-to-location-by-guid.md) | `PUT /inventory-assignment/catalog-guid-location-identifier/:cpcGuid/:targetLocationGuid` | [docs](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1inventory-assignment~1catalog-guid-location-identifier~1{cpcGuid}~1{targetLocationGuid}/put) |
| [Cancel SDS Obtainment](actions/cancel-sds-obtainment.md) | `PUT /customer-action-cancel-obtainment` | [docs](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1customer-action-cancel-obtainment/put) |
| [Create Catalog Item](actions/create-catalog-item.md) | `POST /catalog-item` | [docs](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1catalog-item/post) |
| [Create Catalog Item in Locations](actions/create-catalog-item-in-locations.md) | `POST /catalog-item-inventory` | [docs](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1catalog-item-inventory/post) |
| [Create Catalog Item in Locations with SDS Attachment](actions/create-catalog-item-in-locations-with-sds-attachment.md) | `POST /catalog-item-location-attachment` | [docs](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1catalog-item-location-attachment/post) |
| [Create Catalog Item with SDS Attachment](actions/create-catalog-item-with-sds-attachment.md) | `POST /catalog-item-attachment` | [docs](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1catalog-item-attachment/post) |
| [Create Location](actions/create-location.md) | `POST /location` | [docs](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1location/post) |
| [Deactivate Catalog Item](actions/deactivate-catalog-item.md) | `DELETE /catalog-item/:source/:identifier` | [docs](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1catalog-item~1{source}~1{identifier}/delete) |
| [Delete Location](actions/delete-location.md) | `DELETE /location/:name` | [docs](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1location~1{name}/delete) |
| [Get Catalog Item](actions/get-catalog-item.md) | `GET /catalog-item/:source/:identifier` | [docs](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1catalog-item~1{source}~1{identifier}/get) |
| [Get Catalog Item by GUID](actions/get-catalog-item-by-guid.md) | `GET /catalog-item/guid/:productGuid` | [docs](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1catalog-item~1guid~1{productGuid}/get) |
| [Get Catalog Item by Language and Country](actions/get-catalog-item-by-language-and-country.md) | `GET /catalog-item/:source/:identifier/:locale/:country` | [docs](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1catalog-item~1{source}~1{identifier}~1{locale}~1{country}/get) |
| [Get File](actions/get-file.md) | `GET https://3eonline.com/ImageServer/ImageViewer.aspx` |  |
| [Get Location by GUID](actions/get-location-by-guid.md) | `GET /location/guid/:locationGuid` | [docs](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1location~1guid~1{locationGuid}/get) |
| [Get Location by ID](actions/get-location-by-id.md) | `GET /location/id/:locationId` | [docs](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1location~1id~1{locationId}/get) |
| [Get Location SDS Requirements](actions/get-location-sds-requirements.md) | `GET /location-obtainment/:name` | [docs](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1location-obtainment~1{name}/get) |
| [Link Catalog Item Identifier](actions/link-catalog-item-identifier.md) | `PUT /link-catalog-item/:eeeProductUid/:source/:identifier` | [docs](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1link-catalog-item~1{eeeProductUid}~1{source}~1{identifier}/put) |
| [List Custom Value Names](actions/list-custom-value-names.md) | `GET /custom-value-names` | [docs](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/UniversalDocumentSearch/swagger.json#/paths/~1api~1universaldocumentsearch~1v1~1custom-value-names/get) |
| [List Deactivated Catalog Items](actions/list-deactivated-catalog-items.md) | `GET /deactivated-items/:page` | [docs](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1deactivated-items~1{page}/get) |
| [List Locations](actions/list-locations.md) | `GET /location` | [docs](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1location/get) |
| [List Product Identifier Sources](actions/list-product-identifier-sources.md) | `GET /product-identifier-sources` | [docs](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/UniversalDocumentSearch/swagger.json#/paths/~1api~1universaldocumentsearch~1v1~1product-identifier-sources/get) |
| [List SDS Obtainment Status Changes](actions/list-sds-obtainment-status-changes.md) | `GET /catalog-item-obtainment-status` | [docs](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1catalog-item-obtainment-status/get) |
| [List SDS Obtainment Status Notes](actions/list-sds-obtainment-status-notes.md) | `GET /catalog-item-obtainment-status-notes/:source/:identifier/:locale/:country` | [docs](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1catalog-item-obtainment-status-notes~1{source}~1{identifier}~1{locale}~1{country}/get) |
| [List SDS Requirements](actions/list-sds-requirements.md) | `GET /obtainment-types` | [docs](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1obtainment-types/get) |
| [List Unlinked Catalog Items](actions/list-unlinked-catalog-items.md) | `GET /unlinked-catalog-item/:page/:source` | [docs](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1unlinked-catalog-item~1{page}~1{source}/get) |
| [Remove Catalog Item from Location](actions/remove-catalog-item-from-location.md) | `DELETE /inventory-assignment/unique-identifier-location-uid/:source/:identifier/:targetLocationGuid` | [docs](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1inventory-assignment~1unique-identifier-location-uid~1{source}~1{identifier}~1{targetLocationGuid}/delete) |
| [Remove Catalog Item from Location by GUID](actions/remove-catalog-item-from-location-by-guid.md) | `DELETE /inventory-assignment/catalog-guid-location-identifier/:cpcGuid/:targetLocationGuid` | [docs](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1inventory-assignment~1catalog-guid-location-identifier~1{cpcGuid}~1{targetLocationGuid}/delete) |
| [Remove Catalog Item from Locations](actions/remove-catalog-item-from-locations.md) | `DELETE /catalog-item-inventory` | [docs](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1catalog-item-inventory/delete) |
| [Respond to SDS Customer Action](actions/respond-to-sds-customer-action.md) | `PUT /customer-action-notes-file` | [docs](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1customer-action-notes-file/put) |
| [Search Catalog Items](actions/search-catalog-items.md) | `POST /document-search` | [docs](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/UniversalDocumentSearch/swagger.json#/paths/~1api~1universaldocumentsearch~1v1~1document-search/post) |
| [Set Catalog Item Custom Values](actions/set-catalog-item-custom-values.md) | `PUT /catalog-item/customvalue/:source/:identifier` | [docs](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1catalog-item~1customvalue~1{source}~1{identifier}/put) |
| [Update Catalog Item](actions/update-catalog-item.md) | `PUT /catalog-item` | [docs](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1catalog-item/put) |
| [Update Location](actions/update-location.md) | `PUT /location` | [docs](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1location/put) |
| [Upload SDS Revision](actions/upload-sds-revision.md) | `POST /revision` | [docs](https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/Universal/swagger.json#/paths/~1api~1universal~1v1~1revision/post) |
