# <img src="https://images.mindcloud.co/apps/icons/inventory-base-icon_1776089341563.png" alt="InventoryBase logo" width="28" height="28"> InventoryBase: Universal API

InventoryBase provides property, inspection, report, client, staff, template, webhook, file sharing, and configuration APIs for property inventory and inspection workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/inventoryBase/latest
- **Category:** Support / Field Service
- **Actions:** 41
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://inventorybase.com
- **Vendor API docs:** https://developer.inventorybase.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (41)

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [Create Property Meter](actions/create-property-meter.md) | POST | Creates a new property meter in InventoryBase. |
| [Delete Property Meter](actions/delete-property-meter.md) | DELETE | Deletes an existing property meter from InventoryBase. |
| [Get Property Meter](actions/get-property-meter.md) | GET | Retrieves a property meter from InventoryBase by ID. |
| [List Property Meters](actions/list-property-meters.md) | GET | Retrieves all meters for a property in InventoryBase. |
| [Update Property Meter](actions/update-property-meter.md) | PUT | Updates an existing property meter in InventoryBase. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Inspection Contact](actions/create-inspection-contact.md) | POST | Creates a new contact for an inspection in InventoryBase. |
| [Create Property Contact](actions/create-property-contact.md) | POST | Creates a new contact for a property in InventoryBase. |
| [Delete Inspection Contact](actions/delete-inspection-contact.md) | DELETE | Deletes an existing inspection contact from InventoryBase. |
| [Delete Property Contact](actions/delete-property-contact.md) | DELETE | Deletes an existing property contact from InventoryBase. |
| [List Inspection Contacts](actions/list-inspection-contacts.md) | GET | Retrieves all contacts for an inspection in InventoryBase. |
| [List Property Contacts](actions/list-property-contacts.md) | GET | Retrieves all contacts for a property in InventoryBase. |
| [Update Inspection Contact](actions/update-inspection-contact.md) | PUT | Updates an existing inspection contact in InventoryBase. |
| [Update Property Contact](actions/update-property-contact.md) | PUT | Updates an existing property contact in InventoryBase. |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom Field](actions/create-custom-field.md) | POST | Creates a new custom field in InventoryBase. |
| [Delete Custom Field](actions/delete-custom-field.md) | DELETE | Deletes an existing custom field from InventoryBase. |
| [List Custom Fields](actions/list-custom-fields.md) | GET | Retrieves all custom fields from InventoryBase. |
| [Update Custom Field](actions/update-custom-field.md) | PUT | Updates an existing custom field in InventoryBase. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | POST | Creates a new client in InventoryBase. |
| [Get Client](actions/get-client.md) | GET | Retrieves a client from InventoryBase by ID. |
| [List Clients](actions/list-clients.md) | GET | Retrieves all client records from InventoryBase. |
| [Update Client](actions/update-client.md) | PUT | Updates an existing client in InventoryBase. |

### Employees

| Action | Method | Description |
| --- | --- | --- |
| [Create Staff Member](actions/create-staff-member.md) | POST | Creates a new staff member in InventoryBase. |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user profile from InventoryBase. |
| [Get Staff Member](actions/get-staff-member.md) | GET | Retrieves a staff member from InventoryBase by ID. |
| [List Staff Members](actions/list-staff-members.md) | GET | Retrieves all staff members from InventoryBase. |
| [Update Staff Member](actions/update-staff-member.md) | PUT | Updates an existing staff member in InventoryBase. |

### Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Delete Webhook Listener](actions/delete-webhook-listener.md) | DELETE | Deletes an existing webhook listener from InventoryBase. |
| [Register Webhook Listener](actions/register-webhook-listener.md) | POST | Creates a new webhook listener in InventoryBase. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Create Property](actions/create-property.md) | POST | Creates a new property record in InventoryBase. |
| [Get Property](actions/get-property.md) | GET | Retrieves a property record from InventoryBase by ID. |
| [List Properties](actions/list-properties.md) | GET | Retrieves all property records from InventoryBase. |
| [Update Property](actions/update-property.md) | PUT | Updates an existing property record in InventoryBase. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Create Inspection](actions/create-inspection.md) | POST | Creates a new inspection in InventoryBase. |
| [Get Inspection](actions/get-inspection.md) | GET | Retrieves an inspection from InventoryBase by ID. |
| [Get Inspection Report](actions/get-inspection-report.md) | GET | Retrieves an inspection report from InventoryBase. |
| [Get Inspection Report Metadata](actions/get-inspection-report-metadata.md) | GET | Retrieves inspection report metadata from InventoryBase. |
| [Get Template Report](actions/get-template-report.md) | GET | Retrieves a template report from InventoryBase. |
| [List Action Reports by Inspection](actions/list-action-reports-by-inspection.md) | GET | Retrieves action reports for an inspection in InventoryBase. |
| [List Inspections](actions/list-inspections.md) | GET | Retrieves all inspection records from InventoryBase. |
| [Load Template into Inspection](actions/load-template-into-inspection.md) | PUT | Updates an inspection in InventoryBase by loading a template. |
| [Update Inspection](actions/update-inspection.md) | PUT | Updates an existing inspection in InventoryBase. |

