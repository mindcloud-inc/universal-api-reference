# ShipWise: Native API Reference

A consolidated summary of ShipWise's API configuration and 139 documented operations, with links to official documentation.

- **Official docs:** https://docs.shipwise.com/docs/introduction
- **OpenAPI specification:** https://api.shipwise.com/swagger/v2/swagger.json
- **API base URL:** `https://api.shipwise.com/`

## Authentication

### API Token

Use a ShipWise API token as a Bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://info.shipwise.com/knowledge/shipwise-api)

## API conventions

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (139 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Carrier Service V2](actions/add-carrier-service-v2.md) | `POST /api/v2/CarrierServices/Add` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Add Location V2](actions/add-location-v2.md) | `POST /api/v2/Locations/Add` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Add Marketplace Inbound Mapping V2](actions/add-marketplace-inbound-mapping-v2.md) | `POST /api/v2/Marketplace/InboundMappings/Add` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Add Marketplace Inbound Return Mapping V2](actions/add-marketplace-inbound-return-mapping-v2.md) | `POST /api/v2/Marketplace/InboundReturnMappings/Add` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Add Marketplace Outbound Mapping V2](actions/add-marketplace-outbound-mapping-v2.md) | `POST /api/v2/Marketplace/OutboundMappings/Add` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Add Package To Order V2](actions/add-package-to-order-v2.md) | `POST /api/v2/Order/AddPackageToOrder` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Add Packaging V2](actions/add-packaging-v2.md) | `POST /api/v2/V2Packaging/Add` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Add Profile Resolver V1](actions/add-profile-resolver-v1.md) | `POST /api/v1/Profiles/AddResolver` | [docs](https://api.shipwise.com/swagger/v1/swagger.json) |
| [Add Profile V2](actions/add-profile-v2.md) | `POST /api/v2/V2Profiles/Add` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Add Service Group V2](actions/add-service-group-v2.md) | `POST /api/v2/ServiceGroups/Add` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Add Tax Value Mapping V2](actions/add-tax-value-mapping-v2.md) | `POST /api/v2/TaxValueMappings/Add` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Add Third Party Billing Mapping V2](actions/add-third-party-billing-mapping-v2.md) | `POST /api/v2/ThirdPartyBilling/Add` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Adjust Order Item Package Allocation V2](actions/adjust-order-item-package-allocation-v2.md) | `POST /api/v2/Order/AdjustItemPackageAllocation` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Calculate Packaging Scenarios V2](actions/calculate-packaging-scenarios-v2.md) | `POST /api/v2/Packaging` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Cancel Batch V1](actions/cancel-batch-v1.md) | `GET /api/v1/Batch/:id/Cancel` | [docs](https://api.shipwise.com/swagger/v1/swagger.json) |
| [Check Packaging Automation V2](actions/check-packaging-automation-v2.md) | `POST /api/v2/Packaging/CheckForPackagingAutomation` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Check Shipment Duplicates V1](actions/check-shipment-duplicates-v1.md) | `GET /api/v1/Ship/:id/Check` | [docs](https://api.shipwise.com/swagger/v1/swagger.json) |
| [Close Batch V2](actions/close-batch-v2.md) | `POST /api/v2/V2Batch/Close` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Close Carrier V1](actions/close-carrier-v1.md) | `POST /api/v1/Ship/Close` | [docs](https://api.shipwise.com/swagger/v1/swagger.json) |
| [Continue Shipment Query V1](actions/continue-shipment-query-v1.md) | `GET /api/v1/Ship/Query` | [docs](https://api.shipwise.com/swagger/v1/swagger.json) |
| [Create Batch V1](actions/create-batch-v1.md) | `POST /api/v1/Batch/Create` | [docs](https://api.shipwise.com/swagger/v1/swagger.json) |
| [Create Carton V1](actions/create-carton-v1.md) | `POST /api/v1/Ship/Carton/Create` | [docs](https://api.shipwise.com/swagger/v1/swagger.json) |
| [Create Or Update Product V2](actions/create-or-update-product-v2.md) | `PUT /api/v2/Product/Create` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Create Order V2](actions/create-order-v2.md) | `POST /api/v2/Order/Create` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Create Packaging Automation V2](actions/create-packaging-automation-v2.md) | `POST /api/v2/Packaging/CreatePackagingAutomation` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Create Profile Mapping V1](actions/create-profile-mapping-v1.md) | `POST /api/v1/Profiles/Mapping` | [docs](https://api.shipwise.com/swagger/v1/swagger.json) |
| [Create Shipment Label V1](actions/create-shipment-label-v1.md) | `POST /api/v1/Ship` | [docs](https://api.shipwise.com/swagger/v1/swagger.json) |
| [Delete Location V2](actions/delete-location-v2.md) | `POST /api/v2/Locations/Delete` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Delete Marketplace Inbound Mapping V2](actions/delete-marketplace-inbound-mapping-v2.md) | `POST /api/v2/Marketplace/InboundMappings/Delete` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Delete Marketplace Inbound Return Mapping V2](actions/delete-marketplace-inbound-return-mapping-v2.md) | `POST /api/v2/Marketplace/InboundReturnMappings/Delete` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Delete Marketplace Outbound Mapping V2](actions/delete-marketplace-outbound-mapping-v2.md) | `POST /api/v2/Marketplace/OutboundMappings/Delete` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Delete Packaging V2](actions/delete-packaging-v2.md) | `POST /api/v2/V2Packaging/Delete` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Delete Profile V2](actions/delete-profile-v2.md) | `POST /api/v2/V2Profiles/Delete` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Delete Service Group V2](actions/delete-service-group-v2.md) | `POST /api/v2/ServiceGroups/Delete` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Delete Tax Value Mapping V2](actions/delete-tax-value-mapping-v2.md) | `POST /api/v2/TaxValueMappings/Delete` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Delete Third Party Billing Mapping V2](actions/delete-third-party-billing-mapping-v2.md) | `POST /api/v2/ThirdPartyBilling/Delete` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Edit Carrier Service V2](actions/edit-carrier-service-v2.md) | `PATCH /api/v2/CarrierServices/Edit` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Edit Global Settings V2](actions/edit-global-settings-v2.md) | `PATCH /api/v2/GlobalSettings/Edit` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Edit Location V2](actions/edit-location-v2.md) | `PATCH /api/v2/Locations/Edit` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Edit Packaging V2](actions/edit-packaging-v2.md) | `PATCH /api/v2/V2Packaging/Edit` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Edit Profile V2](actions/edit-profile-v2.md) | `PATCH /api/v2/V2Profiles/Edit` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Edit Service Group V2](actions/edit-service-group-v2.md) | `PATCH /api/v2/ServiceGroups/Edit` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Edit Tax Value Mapping V2](actions/edit-tax-value-mapping-v2.md) | `PATCH /api/v2/TaxValueMappings/Edit` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Edit Third Party Billing Mapping V2](actions/edit-third-party-billing-mapping-v2.md) | `PATCH /api/v2/ThirdPartyBilling/Edit` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Edit User V2](actions/edit-user-v2.md) | `PATCH /api/v2/User/Edit` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Generate Internal Freight BOL V1](actions/generate-internal-freight-bol-v1.md) | `POST /api/v1/Freight/InternalBOL` | [docs](https://api.shipwise.com/swagger/v1/swagger.json) |
| [Get Available Email Preferences V2](actions/get-available-email-preferences-v2.md) | `GET /api/v2/Settings/GetAvailableEmailPreferences` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Get Batch Summary V1](actions/get-batch-summary-v1.md) | `GET /api/v1/Batch/Summary` | [docs](https://api.shipwise.com/swagger/v1/swagger.json) |
| [Get Batch V1](actions/get-batch-v1.md) | `GET /api/v1/Batch/:id` | [docs](https://api.shipwise.com/swagger/v1/swagger.json) |
| [Get Best Email Preference IDs V2](actions/get-best-email-preference-ids-v2.md) | `GET /api/v2/Settings/GetBestEmailPreferenceIds` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Get Channel Settings By Link V2](actions/get-channel-settings-by-link-v2.md) | `GET /api/v2/Channel/:linkId/settings` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Get Close V1](actions/get-close-v1.md) | `GET /api/v1/Ship/Close/:closeId` | [docs](https://api.shipwise.com/swagger/v1/swagger.json) |
| [Get Global Settings V2](actions/get-global-settings-v2.md) | `GET /api/v2/GlobalSettings` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Get Order V2](actions/get-order-v2.md) | `GET /api/v2/Order/:id` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Get Packaging Solution V2](actions/get-packaging-solution-v2.md) | `POST /api/v2/Packaging/PackagingSolution` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Get Packing Slip V1](actions/get-packing-slip-v1.md) | `GET /api/v1/Print/GetPackingslip` | [docs](https://api.shipwise.com/swagger/v1/swagger.json) |
| [Get Partner Logo V2](actions/get-partner-logo-v2.md) | `GET /api/v2/GlobalSettings/PartnerLogo` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Get Partner Theme V2](actions/get-partner-theme-v2.md) | `GET /api/v2/GlobalSettings/PartnerTheme` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Get Post Processing Label V1](actions/get-post-processing-label-v1.md) | `GET /api/v1/Print/PostProcessing/:token` | [docs](https://api.shipwise.com/swagger/v1/swagger.json) |
| [Get Product Chemical Record V2](actions/get-product-chemical-record-v2.md) | `GET /api/v2/Product/ChemicalRecord` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Get Product V2](actions/get-product-v2.md) | `GET /api/v2/Product/:id` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Get Shipment](actions/get-shipment.md) | `GET /api/v1/Ship/:id` | [docs](https://api.shipwise.com/swagger/v1/swagger.json) |
| [Get User V2](actions/get-user-v2.md) | `GET /api/v2/User` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Get WMS Configuration V2](actions/get-wms-configuration-v2.md) | `GET /api/v2/GlobalSettings/WMSConfiguration` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [List Batches V1](actions/list-batches-v1.md) | `GET /api/v1/Batch` | [docs](https://api.shipwise.com/swagger/v1/swagger.json) |
| [List Brokers V2](actions/list-brokers-v2.md) | `GET /api/v2/Settings/GetBrokers` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [List Carrier Account Info V2](actions/list-carrier-account-info-v2.md) | `GET /api/v2/CarrierServices/CarrierAccountInfo` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [List Carrier Service Info V2](actions/list-carrier-service-info-v2.md) | `GET /api/v2/CarrierServices/CarrierServiceInfo` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [List Carrier Services V2](actions/list-carrier-services-v2.md) | `GET /api/v2/CarrierServices` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [List Channel Mappings V2](actions/list-channel-mappings-v2.md) | `GET /api/v2/Channel/:channelId/mappings` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [List Channel Settings V2](actions/list-channel-settings-v2.md) | `GET /api/v2/Channel/settings` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [List Channels](actions/list-channels.md) | `GET /api/v1/Channel` | [docs](https://api.shipwise.com/swagger/v1/swagger.json) |
| [List Channels V2](actions/list-channels-v2.md) | `GET /api/v2/Channel` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [List Close History V1](actions/list-close-history-v1.md) | `GET /api/v1/Ship/Close/History` | [docs](https://api.shipwise.com/swagger/v1/swagger.json) |
| [List Existing Cartons V1](actions/list-existing-cartons-v1.md) | `GET /api/v1/Ship/Carton/Existing` | [docs](https://api.shipwise.com/swagger/v1/swagger.json) |
| [List Freight Services V1](actions/list-freight-services-v1.md) | `GET /api/v1/Freight/GetServices` | [docs](https://api.shipwise.com/swagger/v1/swagger.json) |
| [List Locations V2](actions/list-locations-v2.md) | `GET /api/v2/Locations` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [List Marketplace Inbound Mappings V2](actions/list-marketplace-inbound-mappings-v2.md) | `GET /api/v2/Marketplace/InboundMappings` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [List Marketplace Inbound Return Mappings V2](actions/list-marketplace-inbound-return-mappings-v2.md) | `GET /api/v2/Marketplace/InboundReturnMappings` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [List Marketplace Outbound Mappings V2](actions/list-marketplace-outbound-mappings-v2.md) | `GET /api/v2/Marketplace/OutboundMappings` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [List Marketplaces V2](actions/list-marketplaces-v2.md) | `GET /api/v2/Marketplace` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [List Order Subscribed Filters V2](actions/list-order-subscribed-filters-v2.md) | `GET /api/v2/Order/SubscribedFilters` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [List Orders V2](actions/list-orders-v2.md) | `GET /api/v2/Order` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [List Packaging Catalog V2](actions/list-packaging-catalog-v2.md) | `GET /api/v2/V2Packaging` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [List Packaging V2](actions/list-packaging-v2.md) | `GET /api/v2/Packaging` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [List Products V2](actions/list-products-v2.md) | `GET /api/v2/Product` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [List Profile Advanced Markups V2](actions/list-profile-advanced-markups-v2.md) | `GET /api/v2/V2Profiles/AdvancedMarkups` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [List Profile Linked Carrier Accounts V2](actions/list-profile-linked-carrier-accounts-v2.md) | `GET /api/v2/V2Profiles/LinkedCarrierAccounts` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [List Profile Linked Integrations V2](actions/list-profile-linked-integrations-v2.md) | `GET /api/v2/V2Profiles/LinkedIntegrations` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [List Profiles V1](actions/list-profiles-v1.md) | `GET /api/v1/Profiles` | [docs](https://api.shipwise.com/swagger/v1/swagger.json) |
| [List Profiles V2](actions/list-profiles-v2.md) | `GET /api/v2/V2Profiles` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [List Rate Services V1](actions/list-rate-services-v1.md) | `GET /api/v1/Rate/Service` | [docs](https://api.shipwise.com/swagger/v1/swagger.json) |
| [List Ready Close Carriers V1](actions/list-ready-close-carriers-v1.md) | `GET /api/v1/Ship/Close` | [docs](https://api.shipwise.com/swagger/v1/swagger.json) |
| [List Regions V1](actions/list-regions-v1.md) | `GET /api/v1/Profiles/Regions` | [docs](https://api.shipwise.com/swagger/v1/swagger.json) |
| [List Service Groups V2](actions/list-service-groups-v2.md) | `GET /api/v2/ServiceGroups` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [List Shipments V1](actions/list-shipments-v1.md) | `GET /api/v1/Ship` | [docs](https://api.shipwise.com/swagger/v1/swagger.json) |
| [List Shipping Users V1](actions/list-shipping-users-v1.md) | `GET /api/v1/Ship/Users` | [docs](https://api.shipwise.com/swagger/v1/swagger.json) |
| [List Special Service Info V2](actions/list-special-service-info-v2.md) | `GET /api/v2/CarrierServices/SpecialServiceInfo` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [List Tax Value Mappings V2](actions/list-tax-value-mappings-v2.md) | `GET /api/v2/TaxValueMappings` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [List Third Party Billing Mappings V2](actions/list-third-party-billing-mappings-v2.md) | `GET /api/v2/ThirdPartyBilling` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Mark Order Cancelled V2](actions/mark-order-cancelled-v2.md) | `POST /api/v2/Order/:id/Cancelled` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Mark Order Hold V2](actions/mark-order-hold-v2.md) | `POST /api/v2/Order/:id/Hold` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Mark Order New V2](actions/mark-order-new-v2.md) | `POST /api/v2/Order/:id/New` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Mark Order Shipped V2](actions/mark-order-shipped-v2.md) | `POST /api/v2/Order/:id/Shipped` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Mark Package Printed V1](actions/mark-package-printed-v1.md) | `POST /api/v1/Print/:PackageId/MarkPrinted` | [docs](https://api.shipwise.com/swagger/v1/swagger.json) |
| [Override Profile Advanced Markups V2](actions/override-profile-advanced-markups-v2.md) | `POST /api/v2/V2Profiles/AdvancedMarkups/Override` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Override Profile Linked Carrier Accounts V2](actions/override-profile-linked-carrier-accounts-v2.md) | `POST /api/v2/V2Profiles/LinkedCarrierAccounts/Override` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Override Profile Linked Integrations V2](actions/override-profile-linked-integrations-v2.md) | `POST /api/v2/V2Profiles/LinkedIntegrations/Override` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Print Batch V1](actions/print-batch-v1.md) | `GET /api/v1/Print/PrintBatch` | [docs](https://api.shipwise.com/swagger/v1/swagger.json) |
| [Print By Item V1](actions/print-by-item-v1.md) | `POST /api/v1/Print/ByItem` | [docs](https://api.shipwise.com/swagger/v1/swagger.json) |
| [Print Labels V1](actions/print-labels-v1.md) | `GET /api/v1/Print` | [docs](https://api.shipwise.com/swagger/v1/swagger.json) |
| [Print Labels V2](actions/print-labels-v2.md) | `GET /api/v2/V2Print` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Query Profile Mapping V1](actions/query-profile-mapping-v1.md) | `POST /api/v1/Profiles/Mapping/Query` | [docs](https://api.shipwise.com/swagger/v1/swagger.json) |
| [Query Shipments](actions/query-shipments.md) | `POST /api/v1/Ship/Query` | [docs](https://api.shipwise.com/swagger/v1/swagger.json) |
| [Query Single Order V1](actions/query-single-order-v1.md) | `POST /api/v1/Order/QuerySingle` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Rate And Ship Order V1](actions/rate-and-ship-order-v1.md) | `POST /api/v1/Ship/RateAndShip/:orderId` | [docs](https://api.shipwise.com/swagger/v1/swagger.json) |
| [Rate And Ship V1](actions/rate-and-ship-v1.md) | `POST /api/v1/Ship/RateAndShip` | [docs](https://api.shipwise.com/swagger/v1/swagger.json) |
| [Rate Batch V2](actions/rate-batch-v2.md) | `POST /api/v2/V2Batch/Rate` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Rate Freight V1](actions/rate-freight-v1.md) | `POST /api/v1/Freight/Rate` | [docs](https://api.shipwise.com/swagger/v1/swagger.json) |
| [Rate Order Package V1](actions/rate-order-package-v1.md) | `GET /api/v1/Rate/:orderId` | [docs](https://api.shipwise.com/swagger/v1/swagger.json) |
| [Rate Shipment V1](actions/rate-shipment-v1.md) | `POST /api/v1/Rate` | [docs](https://api.shipwise.com/swagger/v1/swagger.json) |
| [Reprint Close V1](actions/reprint-close-v1.md) | `GET /api/v1/Ship/Close/Reprint` | [docs](https://api.shipwise.com/swagger/v1/swagger.json) |
| [Resolve Country Region V1](actions/resolve-country-region-v1.md) | `GET /api/v1/Profiles/Regions/Resolve/Country` | [docs](https://api.shipwise.com/swagger/v1/swagger.json) |
| [Search Carrier Hold Locations V1](actions/search-carrier-hold-locations-v1.md) | `POST /api/v1/Rate/SearchCarrierHoldLocations` | [docs](https://api.shipwise.com/swagger/v1/swagger.json) |
| [Ship Batch V2](actions/ship-batch-v2.md) | `POST /api/v2/V2Batch/Ship` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Ship Freight V1](actions/ship-freight-v1.md) | `POST /api/v1/Freight/Ship` | [docs](https://api.shipwise.com/swagger/v1/swagger.json) |
| [Simple Ship V2](actions/simple-ship-v2.md) | `POST /api/v2/V2Ship/SimpleShip` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Track Shipment](actions/track-shipment.md) | `GET /api/v1/Ship/Tracking` | [docs](https://api.shipwise.com/swagger/v1/swagger.json) |
| [Unvoid Shipment V1](actions/unvoid-shipment-v1.md) | `GET /api/v1/Ship/:id/UnVoid` | [docs](https://api.shipwise.com/swagger/v1/swagger.json) |
| [Update External Product V2](actions/update-external-product-v2.md) | `PUT /api/v2/Product/UpdateExternal` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Upsert Order Client Reference V2](actions/upsert-order-client-reference-v2.md) | `PUT /api/v2/Order/ClientReference` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Upsert Package Reference V2](actions/upsert-package-reference-v2.md) | `PUT /api/v2/Reference` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Upsert Third Party Billing Account V2](actions/upsert-third-party-billing-account-v2.md) | `PUT /api/v2/ThirdPartyBilling/Upsert` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Validate Token V2](actions/validate-token-v2.md) | `GET /api/v2/Authorize/Validate` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Verify Address For Rate V1](actions/verify-address-for-rate-v1.md) | `POST /api/v1/Rate/AddressVerify` | [docs](https://api.shipwise.com/swagger/v1/swagger.json) |
| [Verify Address For Rate V2](actions/verify-address-for-rate-v2.md) | `POST /api/v2/V2Rate/AddressVerify` | [docs](https://api.shipwise.com/swagger/v2/swagger.json) |
| [Verify International Address For Rate V1](actions/verify-international-address-for-rate-v1.md) | `POST /api/v1/Rate/InternationalAddressVerify` | [docs](https://api.shipwise.com/swagger/v1/swagger.json) |
| [Void Batch V1](actions/void-batch-v1.md) | `GET /api/v1/Batch/:id/Void` | [docs](https://api.shipwise.com/swagger/v1/swagger.json) |
| [Void Shipment V1](actions/void-shipment-v1.md) | `GET /api/v1/Ship/:id/Void` | [docs](https://api.shipwise.com/swagger/v1/swagger.json) |
