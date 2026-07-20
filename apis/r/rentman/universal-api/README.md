# <img src="https://images.mindcloud.co/apps/icons/rentman_1774468578623.png" alt="Rentman logo" width="28" height="28"> Rentman: Universal API

Manage projects, equipment, crew, and invoices in Rentman

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/rentman/latest
- **Category:** Commerce / ERP
- **Actions:** 26
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://rentman.io
- **Vendor API docs:** https://api.rentman.net

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Contacts](actions/list-contacts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rentman/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (26)

### Appointment

| Action | Method | Description |
| --- | --- | --- |
| [Create Appointment](actions/create-appointment.md) | POST |  |
| [Get Appointment](actions/get-appointment.md) | GET |  |
| [List Appointments](actions/list-appointments.md) | GET |  |
| [Update Appointment](actions/update-appointment.md) | PUT |  |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST |  |
| [Get Contact](actions/get-contact.md) | GET |  |
| [List Contacts](actions/list-contacts.md) | GET |  |
| [Update Contact](actions/update-contact.md) | PUT |  |

### Contact Person

| Action | Method | Description |
| --- | --- | --- |
| [List Contact Persons](actions/list-contact-persons.md) | GET |  |

### Crew

| Action | Method | Description |
| --- | --- | --- |
| [Get Crew](actions/get-crew.md) | GET |  |
| [List Crew](actions/list-crew.md) | GET |  |

### Equipment

| Action | Method | Description |
| --- | --- | --- |
| [Get Equipment](actions/get-equipment.md) | GET |  |
| [List Equipment](actions/list-equipment.md) | GET |  |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Get Invoice](actions/get-invoice.md) | GET |  |
| [List Invoices](actions/list-invoices.md) | GET |  |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST |  |
| [Get Project](actions/get-project.md) | GET |  |
| [List Projects](actions/list-projects.md) | GET |  |

### Project Crew

| Action | Method | Description |
| --- | --- | --- |
| [List Project Crew](actions/list-project-crew.md) | GET |  |

### Project Equipment

| Action | Method | Description |
| --- | --- | --- |
| [List Project Equipment](actions/list-project-equipment.md) | GET |  |

### Project Function

| Action | Method | Description |
| --- | --- | --- |
| [Create Project Function](actions/create-project-function.md) | POST |  |
| [List Project Functions](actions/list-project-functions.md) | GET |  |

### Rate

| Action | Method | Description |
| --- | --- | --- |
| [List Crew Rates](actions/list-crew-rates.md) | GET |  |

### Serial Number

| Action | Method | Description |
| --- | --- | --- |
| [List Equipment Serial Numbers](actions/list-equipment-serial-numbers.md) | GET |  |

### Subproject

| Action | Method | Description |
| --- | --- | --- |
| [List Project Subprojects](actions/list-project-subprojects.md) | GET |  |

### Vehicle

| Action | Method | Description |
| --- | --- | --- |
| [List Vehicles](actions/list-vehicles.md) | GET |  |

