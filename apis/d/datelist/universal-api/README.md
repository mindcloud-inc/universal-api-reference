# <img src="https://images.mindcloud.co/apps/icons/datelist_1775039636351.png" alt="Datelist logo" width="28" height="28"> Datelist: Universal API

Datelist is an online scheduling platform API for calendars, products, booked slots, and webhooks.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/datelist/latest
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://datelist.io
- **Vendor API docs:** https://apidoc.datelist.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Calendars](actions/list-calendars.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datelist/latest/actions/list-calendars?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Booked Slot

| Action | Method | Description |
| --- | --- | --- |
| [Delete Booked Slot](actions/delete-booked-slot.md) | DELETE | Cancels an existing booked slot in Datelist. |
| [List Booked Slots](actions/list-booked-slots.md) | GET | Retrieves booked slots from Datelist by email, calendar, or date. |
| [Update Booked Slot](actions/update-booked-slot.md) | PUT | Updates an existing booked slot in Datelist. |

### Calendar

| Action | Method | Description |
| --- | --- | --- |
| [List Calendars](actions/list-calendars.md) | GET | Retrieves available calendars from your Datelist account. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [List Products](actions/list-products.md) | GET | Retrieves available products from Datelist by name or calendar. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Datelist for booking notifications. |

