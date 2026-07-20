# <img src="https://images.mindcloud.co/apps/icons/favicon-trak-codes-48x48_1777042305966.png" alt="Trak Qr Automation logo" width="28" height="28"> Trak Qr Automation: Universal API

Create Trak QR-code events, add attendees, register event partners, and check partner attendee balance through the Trak Events Partner API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/trakQrAutomation/latest
- **Category:** Marketing
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://trak.codes
- **Vendor API docs:** https://docs.google.com/document/u/2/d/e/2PACX-1vSFebcwRE1ntGhoYLQB90Ujf5BfUFocWmZWTfw1FGW3LawP3Q7ZDDOGwHEwsVQnwXJO2tdj1d8NQqit/pub?urp=gmail_link

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Partner Balance](actions/get-partner-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trakQrAutomation/latest/actions/get-partner-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Attendee

| Action | Method | Description |
| --- | --- | --- |
| [Create Attendee](actions/create-attendee.md) | POST | Creates a new attendee for an event in Trak Qr Automation. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Create Event](actions/create-event.md) | POST | Creates a new event in Trak Qr Automation. |

### Partner

| Action | Method | Description |
| --- | --- | --- |
| [Create Partner](actions/create-partner.md) | POST | Creates a new partner in Trak Qr Automation. |

### Partner Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Partner Balance](actions/get-partner-balance.md) | GET | Retrieves partner balance from Trak Qr Automation. |

