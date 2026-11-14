# <img src="https://images.mindcloud.co/apps/icons/e-protect_1794232846835.png" alt="3E Protect logo" width="28" height="28"> 3E Protect: Universal API

Manage chemical inventory, locations, and Safety Data Sheets

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/eProtect/latest
- **Actions:** 38
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.3eco.com/3e-solutions/chemical-workplace-safety/3e-protect/
- **Vendor API docs:** https://secure.3eonline.com/webservices/AccountServicesV2Api/swagger/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Locations](actions/list-locations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eProtect/latest/actions/list-locations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (38)

### Catalog Item

| Action | Method | Description |
| --- | --- | --- |
| [Add Catalog Item Identifiers](actions/add-catalog-item-identifiers.md) | PUT |  |
| [Create Catalog Item](actions/create-catalog-item.md) | POST |  |
| [Create Catalog Item with SDS Attachment](actions/create-catalog-item-with-sds-attachment.md) | POST |  |
| [Deactivate Catalog Item](actions/deactivate-catalog-item.md) | DELETE |  |
| [Get Catalog Item](actions/get-catalog-item.md) | GET |  |
| [Get Catalog Item by GUID](actions/get-catalog-item-by-guid.md) | GET |  |
| [Get Catalog Item by Language and Country](actions/get-catalog-item-by-language-and-country.md) | GET |  |
| [Link Catalog Item Identifier](actions/link-catalog-item-identifier.md) | PUT |  |
| [List Deactivated Catalog Items](actions/list-deactivated-catalog-items.md) | GET |  |
| [List Unlinked Catalog Items](actions/list-unlinked-catalog-items.md) | GET |  |
| [Search Catalog Items](actions/search-catalog-items.md) | GET |  |
| [Set Catalog Item Custom Values](actions/set-catalog-item-custom-values.md) | PUT |  |
| [Update Catalog Item](actions/update-catalog-item.md) | PUT |  |

### Catalog Page

| Action | Method | Description |
| --- | --- | --- |
| [Search Catalog Items Page](actions/search-catalog-items-page.md) | GET |  |

### Custom Field

| Action | Method | Description |
| --- | --- | --- |
| [List Custom Value Names](actions/list-custom-value-names.md) | GET |  |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Get File](actions/get-file.md) | GET | Retrieves a file from the https://3eonline.com/ImageServer/ImageViewer.aspx URL |

### Inventory Assignment

| Action | Method | Description |
| --- | --- | --- |
| [Assign Catalog Item to Location](actions/assign-catalog-item-to-location.md) | PUT |  |
| [Assign Catalog Item to Location by GUID](actions/assign-catalog-item-to-location-by-guid.md) | PUT |  |
| [Create Catalog Item in Locations](actions/create-catalog-item-in-locations.md) | POST |  |
| [Create Catalog Item in Locations with SDS Attachment](actions/create-catalog-item-in-locations-with-sds-attachment.md) | POST |  |
| [Remove Catalog Item from Location](actions/remove-catalog-item-from-location.md) | DELETE |  |
| [Remove Catalog Item from Location by GUID](actions/remove-catalog-item-from-location-by-guid.md) | DELETE |  |
| [Remove Catalog Item from Locations](actions/remove-catalog-item-from-locations.md) | DELETE |  |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [Create Location](actions/create-location.md) | POST |  |
| [Delete Location](actions/delete-location.md) | DELETE |  |
| [Get Location by GUID](actions/get-location-by-guid.md) | GET |  |
| [Get Location by ID](actions/get-location-by-id.md) | GET |  |
| [List Locations](actions/list-locations.md) | GET |  |
| [Update Location](actions/update-location.md) | PUT |  |

### Product Identifier Source

| Action | Method | Description |
| --- | --- | --- |
| [List Product Identifier Sources](actions/list-product-identifier-sources.md) | GET |  |

### Sds Obtainment

| Action | Method | Description |
| --- | --- | --- |
| [Cancel SDS Obtainment](actions/cancel-sds-obtainment.md) | PUT |  |
| [List SDS Obtainment Status Changes](actions/list-sds-obtainment-status-changes.md) | GET |  |
| [List SDS Obtainment Status Notes](actions/list-sds-obtainment-status-notes.md) | GET |  |
| [Respond to SDS Customer Action](actions/respond-to-sds-customer-action.md) | PUT |  |

### Sds Requirement

| Action | Method | Description |
| --- | --- | --- |
| [Add Location SDS Requirement](actions/add-location-sds-requirement.md) | POST |  |
| [Get Location SDS Requirements](actions/get-location-sds-requirements.md) | GET |  |
| [List SDS Requirements](actions/list-sds-requirements.md) | GET |  |

### Sds Revision

| Action | Method | Description |
| --- | --- | --- |
| [Upload SDS Revision](actions/upload-sds-revision.md) | POST |  |

