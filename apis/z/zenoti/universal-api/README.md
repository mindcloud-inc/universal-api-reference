# <img src="https://images.mindcloud.co/apps/icons/zenoti-icon_1782394814458.png" alt="Zenoti logo" width="28" height="28"> Zenoti: Universal API

The AI First platform that helps your business grow

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zenoti/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.zenoti.com/
- **Vendor API docs:** https://docs.zenoti.com/reference/generate-an-access-token

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Centers](actions/list-centers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zenoti/latest/actions/list-centers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Appointments

| Action | Method | Description |
| --- | --- | --- |
| [List Appointments](actions/list-appointments.md) | GET |  |
| [List Appointments By Guest](actions/list-appointments-by-guest.md) | GET |  |
| [Get Appointments Report](actions/list-appointments-flat-file.md) | GET | Returns a simpler result than List Appointments |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Get Guest Details](actions/get-guest-details.md) | GET |  |

### Employees

| Action | Method | Description |
| --- | --- | --- |
| [List Employees](actions/list-employees.md) | GET |  |
| [List Therapists](actions/list-therapists.md) | GET |  |

### Memberships

| Action | Method | Description |
| --- | --- | --- |
| [List Center Membership Details](actions/list-center-membership-details.md) | GET |  |
| [List Guest Memberships](actions/list-guest-memberships.md) | GET |  |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [List Centers](actions/list-centers.md) | GET | This API retrieves an organization's list of active centers. |
| [Get Memberships Report](actions/list-memberships.md) | GET |  |
| [List Services](actions/list-services.md) | GET |  |

### Package Benefit

| Action | Method | Description |
| --- | --- | --- |
| [Get Package Benefits Detail Report](actions/get-package-benefits-detail-report.md) | GET |  |

### Payments

| Action | Method | Description |
| --- | --- | --- |
| [Get Collections Report](actions/list-collections.md) | GET |  |
| [Get Sales Report](actions/list-sales.md) | GET |  |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [List Purchases By Guest](actions/list-purchases-by-guest.md) | GET |  |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Sales Accrual Report](actions/get-sales-accrual-report.md) | GET |  |

### Schedule

| Action | Method | Description |
| --- | --- | --- |
| [List Center Blockout Times](actions/list-center-blockout-times.md) | GET |  |
| [List Center Employee Schedules](actions/list-center-employee-schedules.md) | GET |  |

