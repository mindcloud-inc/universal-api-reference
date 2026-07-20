# <img src="https://images.mindcloud.co/apps/icons/mfr-field-service-management-icon_1777056204127.png" alt="mfr Field Service Management logo" width="28" height="28"> mfr Field Service Management: Universal API

mfr Field Service Management is a cloud platform for dispatching, work order management, service objects, technicians, documents, and related field-service operations. This app wraps the official mfr OData and REST endpoints for read and write automation.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mfrFieldServiceManagement/latest
- **Category:** Support / Field Service
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.mobilefieldreport.com/
- **Vendor API docs:** https://documenter.getpostman.com/view/6932380/2sB3dWsn6U

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Service Requests](actions/list-service-requests.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mfrFieldServiceManagement/latest/actions/list-service-requests?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Appointments

| Action | Method | Description |
| --- | --- | --- |
| [Create Appointment](actions/create-appointment.md) | POST | Creates an appointment in mfr Field Service Management. |
| [List Appointments](actions/list-appointments.md) | GET | Retrieves appointments from mfr Field Service Management. |
| [Update Appointment](actions/update-appointment.md) | PUT | Updates an appointment in mfr Field Service Management. |

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [Create Service Object](actions/create-service-object.md) | POST | Creates a service object in mfr Field Service Management. |
| [Delete Service Object](actions/delete-service-object.md) | DELETE | Deletes a service object from mfr Field Service Management. |
| [Find Service Object by ID](actions/find-service-object-by-id.md) | GET | Finds a service object in mfr Field Service Management by ID. |
| [List Service Objects](actions/list-service-objects.md) | GET | Retrieves service objects from mfr Field Service Management. |
| [List Service Objects by Company](actions/list-service-objects-by-company.md) | GET | Finds service objects in mfr Field Service Management by company. |
| [Update Service Object](actions/update-service-object.md) | PUT | Updates a service object in mfr Field Service Management. |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | POST | Creates a company in mfr Field Service Management. |
| [Find Company by ID](actions/find-company-by-id.md) | GET | Finds a company in mfr Field Service Management by ID. |
| [List Companies](actions/list-companies.md) | GET | Retrieves companies from mfr Field Service Management. |
| [Update Company](actions/update-company.md) | PUT | Updates a company in mfr Field Service Management. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a contact in mfr Field Service Management. |
| [Find Contact by ID](actions/find-contact-by-id.md) | GET | Finds a contact in mfr Field Service Management by ID. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from mfr Field Service Management. |
| [Update Contact](actions/update-contact.md) | PUT | Updates a contact in mfr Field Service Management. |

### Service Requests

| Action | Method | Description |
| --- | --- | --- |
| [Create Service Request](actions/create-service-request.md) | POST | Creates a service request in mfr Field Service Management. |
| [Delete Service Request](actions/delete-service-request.md) | DELETE | Deletes a service request from mfr Field Service Management. |
| [Find Service Request by ID](actions/find-service-request-by-id.md) | GET | Finds a service request in mfr Field Service Management by ID. |
| [List Service Requests](actions/list-service-requests.md) | GET | Retrieves service requests from mfr Field Service Management. |
| [List Service Requests by External ID](actions/list-service-requests-by-external-id.md) | GET | Finds service requests in mfr Field Service Management by external ID. |
| [Update Service Request](actions/update-service-request.md) | PUT | Updates a service request in mfr Field Service Management. |

### Timesheet Entries

| Action | Method | Description |
| --- | --- | --- |
| [List Time Events](actions/list-time-events.md) | GET | Retrieves time events from mfr Field Service Management. |

