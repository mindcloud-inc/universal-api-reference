# <img src="https://images.mindcloud.co/apps/icons/donorbox_1773263176546.png" alt="Donorbox logo" width="28" height="28"> Donorbox: Universal API

Donorbox: Manage campaigns, donors, plans, and donation records

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/donorbox/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://donorbox.org
- **Vendor API docs:** https://github.com/donorbox/donorbox-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Campaigns](actions/list-campaigns.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/donorbox/latest/actions/list-campaigns?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaigns from Donorbox. |

### Donation

| Action | Method | Description |
| --- | --- | --- |
| [List Donations](actions/list-donations.md) | GET | Retrieves donations from Donorbox. |

### Donor

| Action | Method | Description |
| --- | --- | --- |
| [List Donors](actions/list-donors.md) | GET | Retrieves donors from Donorbox. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [List Events](actions/list-events.md) | GET | Retrieves events from Donorbox. |

### Plan

| Action | Method | Description |
| --- | --- | --- |
| [List Plans](actions/list-plans.md) | GET | Retrieves plans from Donorbox. |

### Purchase

| Action | Method | Description |
| --- | --- | --- |
| [List Purchases](actions/list-purchases.md) | GET | Retrieves event ticket purchases from Donorbox. |

### Ticket

| Action | Method | Description |
| --- | --- | --- |
| [List Tickets](actions/list-tickets.md) | GET | Retrieves tickets from Donorbox. |

