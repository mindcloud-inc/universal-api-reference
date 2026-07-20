# <img src="https://images.mindcloud.co/apps/icons/fleetio_1782742767607.png" alt="Fleetio logo" width="28" height="28"> Fleetio: Universal API

Fleetio fleet management API for vehicles, maintenance, fuel, meter tracking, vendors, and contacts.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/fleetio/latest
- **Actions:** 38
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.fleetio.com/
- **Vendor API docs:** https://developer.fleetio.com/docs/api/fleetio-developer-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Vehicles](actions/list-vehicles.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/list-vehicles?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (38)

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Fleetio. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from Fleetio. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves a list of contacts from Fleetio. |
| [Retrieve Contact](actions/retrieve-contact.md) | GET | Retrieves a specific contact from Fleetio. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Fleetio. |

### Fuel Entry

| Action | Method | Description |
| --- | --- | --- |
| [Create Fuel Entry](actions/create-fuel-entry.md) | POST | Creates a new fuel entry in Fleetio. |
| [Delete Fuel Entry](actions/delete-fuel-entry.md) | DELETE | Deletes an existing fuel entry from Fleetio. |
| [List Fuel Entries](actions/list-fuel-entries.md) | GET | Retrieves a list of fuel entries from Fleetio. |
| [Retrieve Fuel Entry](actions/retrieve-fuel-entry.md) | GET | Retrieves a specific fuel entry from Fleetio. |
| [Update Fuel Entry](actions/update-fuel-entry.md) | PUT | Updates an existing fuel entry in Fleetio. |

### Issue

| Action | Method | Description |
| --- | --- | --- |
| [Create Issue](actions/create-issue.md) | POST | Creates a new issue in Fleetio. |
| [Delete Issue](actions/delete-issue.md) | DELETE | Deletes an existing issue from Fleetio. |
| [List Issues](actions/list-issues.md) | GET | Retrieves a list of issues from Fleetio. |
| [Retrieve Issue](actions/retrieve-issue.md) | GET | Retrieves a specific issue from Fleetio. |
| [Update Issue](actions/update-issue.md) | PUT | Updates an existing issue in Fleetio. |

### Meter Entry

| Action | Method | Description |
| --- | --- | --- |
| [Create Meter Entry](actions/create-meter-entry.md) | POST | Creates a new meter entry in Fleetio. |
| [Delete Meter Entry](actions/delete-meter-entry.md) | DELETE | Deletes an existing meter entry from Fleetio. |
| [List Meter Entries](actions/list-meter-entries.md) | GET | Retrieves a list of meter entries from Fleetio. |
| [Retrieve Meter Entry](actions/retrieve-meter-entry.md) | GET | Retrieves a specific meter entry from Fleetio. |

### Service Entry

| Action | Method | Description |
| --- | --- | --- |
| [Create Service Entry](actions/create-service-entry.md) | POST | Creates a new service entry in Fleetio. |
| [List Service Entries](actions/list-service-entries.md) | GET | Retrieves a list of service entries from Fleetio. |
| [Retrieve Service Entry](actions/retrieve-service-entry.md) | GET | Retrieves a specific service entry from Fleetio. |
| [Update Service Entry](actions/update-service-entry.md) | PUT | Updates an existing service entry in Fleetio. |

### Vehicle

| Action | Method | Description |
| --- | --- | --- |
| [Create Vehicle](actions/create-vehicle.md) | POST | Creates a new vehicle in Fleetio. |
| [Delete Vehicle](actions/delete-vehicle.md) | DELETE | Deletes an existing vehicle from Fleetio. |
| [List Vehicles](actions/list-vehicles.md) | GET | Retrieves a list of vehicles from Fleetio. |
| [Retrieve Vehicle](actions/retrieve-vehicle.md) | GET | Retrieves a specific vehicle from Fleetio. |
| [Update Vehicle](actions/update-vehicle.md) | PUT | Updates an existing vehicle in Fleetio. |

### Vendor

| Action | Method | Description |
| --- | --- | --- |
| [Create Vendor](actions/create-vendor.md) | POST | Creates a new vendor in Fleetio. |
| [Delete Vendor](actions/delete-vendor.md) | DELETE | Deletes an existing vendor from Fleetio. |
| [List Vendors](actions/list-vendors.md) | GET | Retrieves a list of vendors from Fleetio. |
| [Retrieve Vendor](actions/retrieve-vendor.md) | GET | Retrieves a specific vendor from Fleetio. |
| [Update Vendor](actions/update-vendor.md) | PUT | Updates an existing vendor in Fleetio. |

### Work Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Work Order](actions/create-work-order.md) | POST | Creates a new work order in Fleetio. |
| [Delete Work Order](actions/delete-work-order.md) | DELETE | Deletes an existing work order from Fleetio. |
| [List Work Orders](actions/list-work-orders.md) | GET | Retrieves a list of work orders from Fleetio. |
| [Retrieve Work Order](actions/retrieve-work-order.md) | GET | Retrieves a specific work order from Fleetio. |
| [Update Work Order](actions/update-work-order.md) | PUT | Updates an existing work order in Fleetio. |

