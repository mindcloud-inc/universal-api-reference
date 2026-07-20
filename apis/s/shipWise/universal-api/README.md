# <img src="https://images.mindcloud.co/apps/icons/ship-wise_1776878462575.png" alt="ShipWise logo" width="28" height="28"> ShipWise: Universal API

ShipWise provides shipping, order, rate, label, tracking, packaging, carrier-service, and marketplace/channel API workflows for high-volume shipping operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/shipWise/latest
- **Category:** Commerce / Supply Chain
- **Actions:** 139
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.shipwise.com/
- **Vendor API docs:** https://docs.shipwise.com/docs/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Validate Token V2](actions/validate-token-v2.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shipWise/latest/actions/validate-token-v2?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (139)

### Access Token

| Action | Method | Description |
| --- | --- | --- |
| [Validate Token V2](actions/validate-token-v2.md) | GET | Validates an API token in ShipWise. |

### Address Verification

| Action | Method | Description |
| --- | --- | --- |
| [Verify Address For Rate V1](actions/verify-address-for-rate-v1.md) | GET | Verifies an address for rating in ShipWise. |
| [Verify Address For Rate V2](actions/verify-address-for-rate-v2.md) | GET | Verifies an address for rating in ShipWise. |

### Batch

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Batch V1](actions/cancel-batch-v1.md) | DELETE | Cancels a batch in ShipWise. |
| [Create Batch V1](actions/create-batch-v1.md) | POST | Creates a batch in ShipWise. |
| [Get Batch V1](actions/get-batch-v1.md) | GET | Retrieves a batch from ShipWise. |
| [List Batches V1](actions/list-batches-v1.md) | GET | Retrieves batches from ShipWise. |
| [Void Batch V1](actions/void-batch-v1.md) | DELETE | Voids a batch in ShipWise. |

### Batch Closeout

| Action | Method | Description |
| --- | --- | --- |
| [Close Batch V2](actions/close-batch-v2.md) | PUT | Closes a batch in ShipWise. |

### Batch Print

| Action | Method | Description |
| --- | --- | --- |
| [Print Batch V1](actions/print-batch-v1.md) | POST | Retrieves printable batch documents from ShipWise. |

### Batch Rate

| Action | Method | Description |
| --- | --- | --- |
| [Rate Batch V2](actions/rate-batch-v2.md) | POST | Retrieves batch rates from ShipWise. |

### Batch Shipment

| Action | Method | Description |
| --- | --- | --- |
| [Ship Batch V2](actions/ship-batch-v2.md) | POST | Ships a batch in ShipWise. |

### Batch Summary

| Action | Method | Description |
| --- | --- | --- |
| [Get Batch Summary V1](actions/get-batch-summary-v1.md) | GET | Retrieves batch summary details from ShipWise. |

### Broker

| Action | Method | Description |
| --- | --- | --- |
| [List Brokers V2](actions/list-brokers-v2.md) | GET | Retrieves brokers from ShipWise. |

### Carrier Account Info

| Action | Method | Description |
| --- | --- | --- |
| [List Carrier Account Info V2](actions/list-carrier-account-info-v2.md) | GET | Retrieves carrier account info from ShipWise. |

### Carrier Closeout

| Action | Method | Description |
| --- | --- | --- |
| [Close Carrier V1](actions/close-carrier-v1.md) | PUT | Closes a carrier in ShipWise. |
| [Get Close V1](actions/get-close-v1.md) | GET | Retrieves a close from ShipWise. |

### Carrier Closeout History

| Action | Method | Description |
| --- | --- | --- |
| [List Close History V1](actions/list-close-history-v1.md) | GET | Retrieves close history from ShipWise. |

### Carrier Closeout Print

| Action | Method | Description |
| --- | --- | --- |
| [Reprint Close V1](actions/reprint-close-v1.md) | POST | Retrieves a printable close document from ShipWise. |

### Carrier Hold Location

| Action | Method | Description |
| --- | --- | --- |
| [Search Carrier Hold Locations V1](actions/search-carrier-hold-locations-v1.md) | GET | Finds carrier hold locations in ShipWise. |

### Carrier Service

| Action | Method | Description |
| --- | --- | --- |
| [Add Carrier Service V2](actions/add-carrier-service-v2.md) | POST | Creates a carrier service in ShipWise. |
| [Edit Carrier Service V2](actions/edit-carrier-service-v2.md) | PUT | Updates a carrier service in ShipWise. |
| [List Carrier Services V2](actions/list-carrier-services-v2.md) | GET | Retrieves carrier services from ShipWise. |

### Carrier Service Info

| Action | Method | Description |
| --- | --- | --- |
| [List Carrier Service Info V2](actions/list-carrier-service-info-v2.md) | GET | Retrieves carrier service info from ShipWise. |

### Carton

| Action | Method | Description |
| --- | --- | --- |
| [Create Carton V1](actions/create-carton-v1.md) | POST | Creates a carton in ShipWise. |
| [List Existing Cartons V1](actions/list-existing-cartons-v1.md) | GET | Retrieves existing cartons from ShipWise. |

### Channel

| Action | Method | Description |
| --- | --- | --- |
| [List Channels](actions/list-channels.md) | GET | Retrieves channels from ShipWise. |
| [List Channels V2](actions/list-channels-v2.md) | GET | Retrieves channels from ShipWise. |

### Channel Mapping

| Action | Method | Description |
| --- | --- | --- |
| [List Channel Mappings V2](actions/list-channel-mappings-v2.md) | GET | Retrieves channel mappings from ShipWise. |

### Channel Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get Channel Settings By Link V2](actions/get-channel-settings-by-link-v2.md) | GET | Retrieves channel settings by link from ShipWise. |
| [List Channel Settings V2](actions/list-channel-settings-v2.md) | GET | Retrieves channel settings from ShipWise. |

### Close Carrier

| Action | Method | Description |
| --- | --- | --- |
| [List Ready Close Carriers V1](actions/list-ready-close-carriers-v1.md) | GET | Retrieves ready close carriers from ShipWise. |

### Email Preference

| Action | Method | Description |
| --- | --- | --- |
| [Get Available Email Preferences V2](actions/get-available-email-preferences-v2.md) | GET | Retrieves available email preferences from ShipWise. |
| [Get Best Email Preference IDs V2](actions/get-best-email-preference-ids-v2.md) | GET | Retrieves recommended email preference IDs from ShipWise. |

### Freight Bol

| Action | Method | Description |
| --- | --- | --- |
| [Generate Internal Freight BOL V1](actions/generate-internal-freight-bol-v1.md) | POST | Retrieves an internal freight BOL from ShipWise. |

### Freight Rate

| Action | Method | Description |
| --- | --- | --- |
| [Rate Freight V1](actions/rate-freight-v1.md) | GET | Retrieves freight rates from ShipWise. |

### Freight Service

| Action | Method | Description |
| --- | --- | --- |
| [List Freight Services V1](actions/list-freight-services-v1.md) | GET | Retrieves freight services from ShipWise. |

### Freight Shipment

| Action | Method | Description |
| --- | --- | --- |
| [Ship Freight V1](actions/ship-freight-v1.md) | POST | Ships freight in ShipWise. |

### Global Settings

| Action | Method | Description |
| --- | --- | --- |
| [Edit Global Settings V2](actions/edit-global-settings-v2.md) | PUT | Updates global settings in ShipWise. |
| [Get Global Settings V2](actions/get-global-settings-v2.md) | GET | Retrieves global settings from ShipWise. |

### International Address Verification

| Action | Method | Description |
| --- | --- | --- |
| [Verify International Address For Rate V1](actions/verify-international-address-for-rate-v1.md) | GET | Verifies an international address for rating in ShipWise. |

### Label Print

| Action | Method | Description |
| --- | --- | --- |
| [Print By Item V1](actions/print-by-item-v1.md) | POST | Retrieves item print output from ShipWise. |
| [Print Labels V1](actions/print-labels-v1.md) | POST | Retrieves printable labels from ShipWise. |
| [Print Labels V2](actions/print-labels-v2.md) | POST | Retrieves printable labels from ShipWise. |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [Add Location V2](actions/add-location-v2.md) | POST | Creates a location in ShipWise. |
| [Delete Location V2](actions/delete-location-v2.md) | DELETE | Deletes a location from ShipWise. |
| [Edit Location V2](actions/edit-location-v2.md) | PUT | Updates a location in ShipWise. |
| [List Locations V2](actions/list-locations-v2.md) | GET | Retrieves locations from ShipWise. |

### Marketplace

| Action | Method | Description |
| --- | --- | --- |
| [List Marketplaces V2](actions/list-marketplaces-v2.md) | GET | Retrieves marketplaces from ShipWise. |

### Marketplace Inbound Mapping

| Action | Method | Description |
| --- | --- | --- |
| [Add Marketplace Inbound Mapping V2](actions/add-marketplace-inbound-mapping-v2.md) | POST | Creates a marketplace inbound mapping in ShipWise. |
| [Delete Marketplace Inbound Mapping V2](actions/delete-marketplace-inbound-mapping-v2.md) | DELETE | Deletes a marketplace inbound mapping from ShipWise. |
| [List Marketplace Inbound Mappings V2](actions/list-marketplace-inbound-mappings-v2.md) | GET | Retrieves marketplace inbound mappings from ShipWise. |

### Marketplace Inbound Return Mapping

| Action | Method | Description |
| --- | --- | --- |
| [Add Marketplace Inbound Return Mapping V2](actions/add-marketplace-inbound-return-mapping-v2.md) | POST | Creates a marketplace inbound return mapping in ShipWise. |
| [Delete Marketplace Inbound Return Mapping V2](actions/delete-marketplace-inbound-return-mapping-v2.md) | DELETE | Deletes a marketplace inbound return mapping from ShipWise. |
| [List Marketplace Inbound Return Mappings V2](actions/list-marketplace-inbound-return-mappings-v2.md) | GET | Retrieves marketplace inbound return mappings from ShipWise. |

### Marketplace Outbound Mapping

| Action | Method | Description |
| --- | --- | --- |
| [Add Marketplace Outbound Mapping V2](actions/add-marketplace-outbound-mapping-v2.md) | POST | Creates a marketplace outbound mapping in ShipWise. |
| [Delete Marketplace Outbound Mapping V2](actions/delete-marketplace-outbound-mapping-v2.md) | DELETE | Deletes a marketplace outbound mapping from ShipWise. |
| [List Marketplace Outbound Mappings V2](actions/list-marketplace-outbound-mappings-v2.md) | GET | Retrieves marketplace outbound mappings from ShipWise. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Add Package To Order V2](actions/add-package-to-order-v2.md) | PUT | Adds a package to an order in ShipWise. |
| [Adjust Order Item Package Allocation V2](actions/adjust-order-item-package-allocation-v2.md) | PUT | Updates order item package allocation in ShipWise. |
| [Create Order V2](actions/create-order-v2.md) | POST | Creates an order in ShipWise. |
| [Get Order V2](actions/get-order-v2.md) | GET | Retrieves an order from ShipWise. |
| [List Orders V2](actions/list-orders-v2.md) | GET | Retrieves orders from ShipWise. |
| [Mark Order Cancelled V2](actions/mark-order-cancelled-v2.md) | PUT | Updates an order to cancelled status in ShipWise. |
| [Mark Order Hold V2](actions/mark-order-hold-v2.md) | PUT | Updates an order to hold status in ShipWise. |
| [Mark Order New V2](actions/mark-order-new-v2.md) | PUT | Updates an order to new status in ShipWise. |
| [Mark Order Shipped V2](actions/mark-order-shipped-v2.md) | PUT | Updates an order to shipped status in ShipWise. |
| [Query Single Order V1](actions/query-single-order-v1.md) | GET | Finds an order in ShipWise by query. |
| [Upsert Order Client Reference V2](actions/upsert-order-client-reference-v2.md) | PUT | Creates or updates an order client reference in ShipWise. |

### Order Subscribed Filter

| Action | Method | Description |
| --- | --- | --- |
| [List Order Subscribed Filters V2](actions/list-order-subscribed-filters-v2.md) | GET | Retrieves order subscribed filters from ShipWise. |

### Package Print Status

| Action | Method | Description |
| --- | --- | --- |
| [Mark Package Printed V1](actions/mark-package-printed-v1.md) | PUT | Updates a package to printed status in ShipWise. |

### Package Reference

| Action | Method | Description |
| --- | --- | --- |
| [Upsert Package Reference V2](actions/upsert-package-reference-v2.md) | PUT | Creates or updates a package reference in ShipWise. |

### Packaging

| Action | Method | Description |
| --- | --- | --- |
| [Add Packaging V2](actions/add-packaging-v2.md) | POST | Creates packaging in ShipWise. |
| [Delete Packaging V2](actions/delete-packaging-v2.md) | DELETE | Deletes packaging from ShipWise. |
| [Edit Packaging V2](actions/edit-packaging-v2.md) | PUT | Updates packaging in ShipWise. |
| [List Packaging Catalog V2](actions/list-packaging-catalog-v2.md) | GET | Retrieves packaging catalog from ShipWise. |
| [List Packaging V2](actions/list-packaging-v2.md) | GET | Retrieves packaging from ShipWise. |

### Packaging Automation

| Action | Method | Description |
| --- | --- | --- |
| [Check Packaging Automation V2](actions/check-packaging-automation-v2.md) | GET | Checks packaging automation in ShipWise. |
| [Create Packaging Automation V2](actions/create-packaging-automation-v2.md) | POST | Creates a packaging automation in ShipWise. |

### Packaging Scenario

| Action | Method | Description |
| --- | --- | --- |
| [Calculate Packaging Scenarios V2](actions/calculate-packaging-scenarios-v2.md) | GET | Retrieves packaging scenarios from ShipWise. |

### Packaging Solution

| Action | Method | Description |
| --- | --- | --- |
| [Get Packaging Solution V2](actions/get-packaging-solution-v2.md) | GET | Retrieves a packaging solution from ShipWise. |

### Packing Slip

| Action | Method | Description |
| --- | --- | --- |
| [Get Packing Slip V1](actions/get-packing-slip-v1.md) | GET | Retrieves a packing slip from ShipWise. |

### Partner Logo

| Action | Method | Description |
| --- | --- | --- |
| [Get Partner Logo V2](actions/get-partner-logo-v2.md) | GET | Retrieves the partner logo from ShipWise. |

### Partner Theme

| Action | Method | Description |
| --- | --- | --- |
| [Get Partner Theme V2](actions/get-partner-theme-v2.md) | GET | Retrieves the partner theme from ShipWise. |

### Post Processing Label

| Action | Method | Description |
| --- | --- | --- |
| [Get Post Processing Label V1](actions/get-post-processing-label-v1.md) | GET | Retrieves a post-processing label from ShipWise. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Create Or Update Product V2](actions/create-or-update-product-v2.md) | PUT | Creates or updates a product in ShipWise. |
| [Get Product V2](actions/get-product-v2.md) | GET | Retrieves a product from ShipWise. |
| [List Products V2](actions/list-products-v2.md) | GET | Retrieves products from ShipWise. |
| [Update External Product V2](actions/update-external-product-v2.md) | PUT | Updates an external product in ShipWise. |

### Product Chemical Record

| Action | Method | Description |
| --- | --- | --- |
| [Get Product Chemical Record V2](actions/get-product-chemical-record-v2.md) | GET | Retrieves a product chemical record from ShipWise. |

### Profile

| Action | Method | Description |
| --- | --- | --- |
| [Add Profile V2](actions/add-profile-v2.md) | POST | Creates a profile in ShipWise. |
| [Delete Profile V2](actions/delete-profile-v2.md) | DELETE | Deletes a profile from ShipWise. |
| [Edit Profile V2](actions/edit-profile-v2.md) | PUT | Updates a profile in ShipWise. |
| [List Profiles V1](actions/list-profiles-v1.md) | GET | Retrieves profiles from ShipWise. |
| [List Profiles V2](actions/list-profiles-v2.md) | GET | Retrieves profiles from ShipWise. |

### Profile Advanced Markup

| Action | Method | Description |
| --- | --- | --- |
| [List Profile Advanced Markups V2](actions/list-profile-advanced-markups-v2.md) | GET | Retrieves profile advanced markups from ShipWise. |
| [Override Profile Advanced Markups V2](actions/override-profile-advanced-markups-v2.md) | PUT | Replaces profile advanced markups in ShipWise. |

### Profile Linked Carrier Account

| Action | Method | Description |
| --- | --- | --- |
| [List Profile Linked Carrier Accounts V2](actions/list-profile-linked-carrier-accounts-v2.md) | GET | Retrieves profile linked carrier accounts from ShipWise. |
| [Override Profile Linked Carrier Accounts V2](actions/override-profile-linked-carrier-accounts-v2.md) | PUT | Replaces profile linked carrier accounts in ShipWise. |

### Profile Linked Integration

| Action | Method | Description |
| --- | --- | --- |
| [List Profile Linked Integrations V2](actions/list-profile-linked-integrations-v2.md) | GET | Retrieves profile linked integrations from ShipWise. |
| [Override Profile Linked Integrations V2](actions/override-profile-linked-integrations-v2.md) | PUT | Replaces profile linked integrations in ShipWise. |

### Profile Mapping

| Action | Method | Description |
| --- | --- | --- |
| [Create Profile Mapping V1](actions/create-profile-mapping-v1.md) | POST | Creates a profile mapping in ShipWise. |
| [Query Profile Mapping V1](actions/query-profile-mapping-v1.md) | GET | Finds profile mapping in ShipWise by query. |

### Profile Resolver

| Action | Method | Description |
| --- | --- | --- |
| [Add Profile Resolver V1](actions/add-profile-resolver-v1.md) | POST | Creates a profile resolver in ShipWise. |

### Rate

| Action | Method | Description |
| --- | --- | --- |
| [Rate Order Package V1](actions/rate-order-package-v1.md) | GET | Retrieves rates for an order package in ShipWise. |
| [Rate Shipment V1](actions/rate-shipment-v1.md) | GET | Retrieves rates for a shipment in ShipWise. |

### Rate Service

| Action | Method | Description |
| --- | --- | --- |
| [List Rate Services V1](actions/list-rate-services-v1.md) | GET | Retrieves rate services from ShipWise. |

### Region

| Action | Method | Description |
| --- | --- | --- |
| [List Regions V1](actions/list-regions-v1.md) | GET | Retrieves regions from ShipWise. |
| [Resolve Country Region V1](actions/resolve-country-region-v1.md) | GET | Finds a country region in ShipWise. |

### Service Group

| Action | Method | Description |
| --- | --- | --- |
| [Add Service Group V2](actions/add-service-group-v2.md) | POST | Creates a service group in ShipWise. |
| [Delete Service Group V2](actions/delete-service-group-v2.md) | DELETE | Deletes a service group from ShipWise. |
| [Edit Service Group V2](actions/edit-service-group-v2.md) | PUT | Updates a service group in ShipWise. |
| [List Service Groups V2](actions/list-service-groups-v2.md) | GET | Retrieves service groups from ShipWise. |

### Shipment

| Action | Method | Description |
| --- | --- | --- |
| [Check Shipment Duplicates V1](actions/check-shipment-duplicates-v1.md) | GET | Checks for shipment duplicates in ShipWise. |
| [Continue Shipment Query V1](actions/continue-shipment-query-v1.md) | GET | Continues a shipment query in ShipWise. |
| [Create Shipment Label V1](actions/create-shipment-label-v1.md) | POST | Creates a shipment label in ShipWise. |
| [Get Shipment](actions/get-shipment.md) | GET | Retrieves a shipment from ShipWise. |
| [List Shipments V1](actions/list-shipments-v1.md) | GET | Retrieves shipments from ShipWise. |
| [Query Shipments](actions/query-shipments.md) | GET | Finds shipments in ShipWise by query. |
| [Rate And Ship Order V1](actions/rate-and-ship-order-v1.md) | POST | Rates and ships an order in ShipWise. |
| [Rate And Ship V1](actions/rate-and-ship-v1.md) | POST | Rates and ships a shipment in ShipWise. |
| [Simple Ship V2](actions/simple-ship-v2.md) | POST | Ships a package in ShipWise. |
| [Track Shipment](actions/track-shipment.md) | GET | Retrieves shipment tracking details from ShipWise. |
| [Unvoid Shipment V1](actions/unvoid-shipment-v1.md) | PUT | Restores a voided shipment in ShipWise. |
| [Void Shipment V1](actions/void-shipment-v1.md) | DELETE | Voids a shipment in ShipWise. |

### Shipping User

| Action | Method | Description |
| --- | --- | --- |
| [List Shipping Users V1](actions/list-shipping-users-v1.md) | GET | Retrieves shipping users from ShipWise. |

### Special Service Info

| Action | Method | Description |
| --- | --- | --- |
| [List Special Service Info V2](actions/list-special-service-info-v2.md) | GET | Retrieves special service info from ShipWise. |

### Tax Value Mapping

| Action | Method | Description |
| --- | --- | --- |
| [Add Tax Value Mapping V2](actions/add-tax-value-mapping-v2.md) | POST | Creates a tax value mapping in ShipWise. |
| [Delete Tax Value Mapping V2](actions/delete-tax-value-mapping-v2.md) | DELETE | Deletes a tax value mapping from ShipWise. |
| [Edit Tax Value Mapping V2](actions/edit-tax-value-mapping-v2.md) | PUT | Updates a tax value mapping in ShipWise. |
| [List Tax Value Mappings V2](actions/list-tax-value-mappings-v2.md) | GET | Retrieves tax value mappings from ShipWise. |

### Third Party Billing Account

| Action | Method | Description |
| --- | --- | --- |
| [Upsert Third Party Billing Account V2](actions/upsert-third-party-billing-account-v2.md) | PUT | Creates or updates a third party billing account in ShipWise. |

### Third Party Billing Mapping

| Action | Method | Description |
| --- | --- | --- |
| [Add Third Party Billing Mapping V2](actions/add-third-party-billing-mapping-v2.md) | POST | Creates a third party billing mapping in ShipWise. |
| [Delete Third Party Billing Mapping V2](actions/delete-third-party-billing-mapping-v2.md) | DELETE | Deletes a third party billing mapping from ShipWise. |
| [Edit Third Party Billing Mapping V2](actions/edit-third-party-billing-mapping-v2.md) | PUT | Updates a third party billing mapping in ShipWise. |
| [List Third Party Billing Mappings V2](actions/list-third-party-billing-mappings-v2.md) | GET | Retrieves third party billing mappings from ShipWise. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Edit User V2](actions/edit-user-v2.md) | PUT | Updates a user in ShipWise. |
| [Get User V2](actions/get-user-v2.md) | GET | Retrieves a user from ShipWise. |

### Wms Configuration

| Action | Method | Description |
| --- | --- | --- |
| [Get WMS Configuration V2](actions/get-wms-configuration-v2.md) | GET | Retrieves WMS configuration from ShipWise. |

