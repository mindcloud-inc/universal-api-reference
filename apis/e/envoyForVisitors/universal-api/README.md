# <img src="https://images.mindcloud.co/apps/icons/envoy-for-visitors_1774370998088.png" alt="Envoy for Visitors logo" width="28" height="28"> Envoy for Visitors: Universal API

Connect Envoy visitor and workplace data to read locations, employees, flows, entries, invites, and work schedules from Cirra.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/envoyForVisitors/latest
- **Category:** Productivity / Scheduling
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://envoy.com
- **Vendor API docs:** https://developers.envoy.com/hub/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Locations](actions/list-locations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/envoyForVisitors/latest/actions/list-locations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Get Company](actions/get-company.md) | GET | Retrieves company details from Envoy for Visitors. |

### Employees

| Action | Method | Description |
| --- | --- | --- |
| [Get Employee](actions/get-employee.md) | GET | Retrieves an employee from Envoy for Visitors. |
| [List Employees](actions/list-employees.md) | GET | Finds employees in Envoy for Visitors. |

### Entry

| Action | Method | Description |
| --- | --- | --- |
| [Create Entry](actions/create-entry.md) | POST | Creates a new entry in Envoy for Visitors. |
| [Get Entry](actions/get-entry.md) | GET | Retrieves an entry from Envoy for Visitors. |
| [List Entries](actions/list-entries.md) | GET | Finds entries in Envoy for Visitors. |
| [Update Entry](actions/update-entry.md) | PUT | Updates an existing entry in Envoy for Visitors. |

### Flow

| Action | Method | Description |
| --- | --- | --- |
| [Get Flow](actions/get-flow.md) | GET | Retrieves a flow from Envoy for Visitors. |
| [List Flows](actions/list-flows.md) | GET | Finds flows in Envoy for Visitors. |

### Invite

| Action | Method | Description |
| --- | --- | --- |
| [Check In Invite](actions/check-in-invite.md) | PUT | Checks in a visitor from an invite in Envoy for Visitors. |
| [Create Invite](actions/create-invite.md) | POST | Creates a new invite in Envoy for Visitors. |
| [Delete Invite](actions/delete-invite.md) | DELETE | Deletes an existing invite from Envoy for Visitors. |
| [Get Invite](actions/get-invite.md) | GET | Retrieves an invite from Envoy for Visitors. |
| [List Invites](actions/list-invites.md) | GET | Finds invites in Envoy for Visitors. |
| [Update Invite](actions/update-invite.md) | PUT | Updates an existing invite in Envoy for Visitors. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Get Location](actions/get-location.md) | GET | Retrieves a location from Envoy for Visitors. |
| [List Locations](actions/list-locations.md) | GET | Retrieves locations from Envoy for Visitors. |

### Recurring Invite

| Action | Method | Description |
| --- | --- | --- |
| [Create Recurring Invite](actions/create-recurring-invite.md) | POST | Creates a new recurring invite in Envoy for Visitors. |
| [Get Recurring Invite](actions/get-recurring-invite.md) | GET | Retrieves a recurring invite from Envoy for Visitors. |
| [Update Recurring Invite](actions/update-recurring-invite.md) | PUT | Updates an existing recurring invite in Envoy for Visitors. |

### Schedules

| Action | Method | Description |
| --- | --- | --- |
| [Check In Work Schedule](actions/check-in-work-schedule.md) | PUT | Checks in a work schedule in Envoy for Visitors. |
| [Check Out Work Schedule](actions/check-out-work-schedule.md) | PUT | Checks out a work schedule in Envoy for Visitors. |
| [Create Work Schedule](actions/create-work-schedule.md) | POST | Creates a new work schedule in Envoy for Visitors. |
| [List Work Schedules](actions/list-work-schedules.md) | GET | Retrieves work schedules from Envoy for Visitors. |

