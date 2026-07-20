# <img src="https://images.mindcloud.co/apps/icons/favicon-32x32_1774906080242.png" alt="Quilia logo" width="28" height="28"> Quilia: Universal API

Quilia is a HIPAA-compliant client manager for law firms. It helps firms remind clients about appointments, track treatment, collect documents, and sync client activity with case management systems.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/quilia/latest
- **Category:** Productivity / Legal & Contracts
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.quilia.com
- **Vendor API docs:** https://api.quilia.dev/v2

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current API Key Information](actions/get-current-api-key-information.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quilia/latest/actions/get-current-api-key-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Api Key Information

| Action | Method | Description |
| --- | --- | --- |
| [Get Current API Key Information](actions/get-current-api-key-information.md) | GET |  |

### Appointments

| Action | Method | Description |
| --- | --- | --- |
| [Create Appointment](actions/create-appointment.md) | POST |  |
| [Delete Appointment](actions/delete-appointment.md) | DELETE |  |
| [Get Appointment](actions/get-appointment.md) | GET |  |
| [Update Appointment](actions/update-appointment.md) | PUT |  |

### Cases

| Action | Method | Description |
| --- | --- | --- |
| [Create Case](actions/create-case.md) | POST |  |
| [Delete Case](actions/delete-case.md) | DELETE |  |
| [Get Case](actions/get-case.md) | GET |  |
| [List Case Types](actions/list-case-types.md) | GET |  |
| [List Cases](actions/list-cases.md) | GET |  |
| [Update Case Details](actions/update-case-details.md) | PUT |  |
| [Update Case Phase](actions/update-case-phase.md) | PUT |  |

### Client

| Action | Method | Description |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | POST |  |
| [Delete Client](actions/delete-client.md) | DELETE |  |
| [List Clients](actions/list-clients.md) | GET |  |
| [Lookup Client By Email Or Phone](actions/lookup-client-by-email-or-phone.md) | GET |  |
| [Update Client Information](actions/update-client-information.md) | PUT |  |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST |  |
| [Delete Contact](actions/delete-contact.md) | DELETE |  |
| [Get Contact](actions/get-contact.md) | GET |  |
| [Update Contact](actions/update-contact.md) | PUT |  |

