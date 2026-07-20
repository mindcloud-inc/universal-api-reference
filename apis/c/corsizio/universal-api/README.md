# <img src="https://images.mindcloud.co/apps/icons/corsizio_1773866663159.png" alt="Corsizio logo" width="28" height="28"> Corsizio: Universal API

Manage Corsizio events, attendees, registrations, and payments

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/corsizio/latest
- **Category:** Marketing / Events & Webinars
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.corsizio.com
- **Vendor API docs:** https://help.corsizio.com/category/28-developer-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Details](actions/get-account-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/corsizio/latest/actions/get-account-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Details](actions/get-account-details.md) | GET | Retrieves account details from a Corsizio account. |

### Attendee

| Action | Method | Description |
| --- | --- | --- |
| [Get Attendee Details](actions/get-attendee-details.md) | GET | Retrieves an attendee from Corsizio by ID. |
| [List Attendees](actions/list-attendees.md) | GET | Retrieves attendees from a Corsizio account. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Event Details](actions/get-event-details.md) | GET | Retrieves an event from Corsizio by ID. |
| [List Events](actions/list-events.md) | GET | Retrieves events from a Corsizio account. |

