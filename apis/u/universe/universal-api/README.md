# <img src="https://images.mindcloud.co/apps/icons/universe_1773952464739.png" alt="Universe logo" width="28" height="28"> Universe: Universal API

Universe GraphQL integration for hosts, events, attendees, orders, discount codes, access keys, rates, categories, countries, and check-in workflows. The app includes 34 actions with live-validated QA coverage plus clearly documented in-development endpoints that still require account permissions or fixture data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/universe/latest
- **Category:** Support / Ticketing
- **Actions:** 34
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.universe.com/
- **Vendor API docs:** https://developers.universe.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Viewer](actions/get-viewer.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/universe/latest/actions/get-viewer?connectionId=$CONNECTION_ID&query=query%20%7B%20viewer%20%7B%20id%20firstName%20lastName%20memberships%20%7B%20nodes%20%7B%20id%20owner%20%7B%20id%20name%20%7D%20%7D%20%7D%20%7D%20%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (34)

### Accesstoken

| Action | Method | Description |
| --- | --- | --- |
| [List Event Access Keys](actions/list-event-access-keys.md) | GET | Retrieves access keys for a specific Universe event. |

### Address

| Action | Method | Description |
| --- | --- | --- |
| [List Stripe Countries](actions/list-stripe-countries.md) | GET | Retrieves available Stripe countries from Universe. |
| [List Whitelisted Countries](actions/list-whitelisted-countries.md) | GET | Retrieves the whitelisted countries from Universe. |

### Attendee

| Action | Method | Description |
| --- | --- | --- |
| [List Event Attendees](actions/list-event-attendees.md) | GET | Retrieves attendees for a specific Universe event. |
| [List Host Attendees](actions/list-host-attendees.md) | GET | Retrieves attendees for a specified Universe host. |

### Calendar

| Action | Method | Description |
| --- | --- | --- |
| [List Calendar Widgets](actions/list-calendar-widgets.md) | GET | Retrieves calendar widgets for a Universe host. |

### Category

| Action | Method | Description |
| --- | --- | --- |
| [List Categories](actions/list-categories.md) | GET | Retrieves the available categories from Universe. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Get Host](actions/get-host.md) | GET | Retrieves a specific host from Universe. |

### Discount

| Action | Method | Description |
| --- | --- | --- |
| [Get Discount](actions/get-discount.md) | GET | Retrieves a specific discount from Universe. |
| [List Event Discount Codes](actions/list-event-discount-codes.md) | GET | Retrieves discount codes for a specific Universe event. |
| [Upsert Event Discounts](actions/upsert-event-discounts.md) | PUT | Creates or updates discounts for a Universe event. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Event](actions/get-event.md) | GET | Retrieves a specific event from Universe. |
| [List Events](actions/list-events.md) | GET | Retrieves events for a specified Universe host. |
| [List Host Events With Tickets](actions/list-host-events-with-tickets.md) | GET | Retrieves ticketed events for a specified Universe host. |

### Membership

| Action | Method | Description |
| --- | --- | --- |
| [Get Membership](actions/get-membership.md) | GET | Retrieves a specific membership from Universe. |
| [List Memberships](actions/list-memberships.md) | GET | Retrieves memberships for the authenticated viewer in Universe. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Get Order](actions/get-order.md) | GET | Retrieves a specific order from Universe. |
| [List Event Orders](actions/list-event-orders.md) | GET | Retrieves orders for a specific Universe event. |
| [List Host Orders](actions/list-host-orders.md) | GET | Retrieves orders for a specified Universe host. |

### Permission

| Action | Method | Description |
| --- | --- | --- |
| [List Available Permissions](actions/list-available-permissions.md) | GET | Retrieves the available permissions from Universe. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Event Report](actions/get-event-report.md) | GET | Retrieves the report preview for a Universe event. |
| [Get Host Report](actions/get-host-report.md) | GET | Retrieves the report preview for a Universe host. |

### Screeningquestion

| Action | Method | Description |
| --- | --- | --- |
| [List Event Questions](actions/list-event-questions.md) | GET | Retrieves attendee questions for a specific Universe event. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Get Default Email Template](actions/get-default-email-template.md) | GET | Retrieves the default email template from Universe. |
| [List Email Templates](actions/list-email-templates.md) | GET | Retrieves the email templates from Universe. |

### Ticket

| Action | Method | Description |
| --- | --- | --- |
| [Check In Order Item](actions/check-in-order-item.md) | PUT | Checks in a specific Universe order item. |
| [Check Out Order Item](actions/check-out-order-item.md) | PUT | Checks out a specific Universe order item. |
| [Get Order Item](actions/get-order-item.md) | GET | Retrieves a specific order item from Universe. |
| [List Event Rates](actions/list-event-rates.md) | GET | Retrieves ticket rates for a specific Universe event. |

### Unknownobject

| Action | Method | Description |
| --- | --- | --- |
| [List Event Referral Codes](actions/list-event-referral-codes.md) | GET | Retrieves referral codes for a specific Universe event. |
| [List Stripe Currencies](actions/list-stripe-currencies.md) | GET | Retrieves available Stripe currencies from Universe. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Viewer](actions/get-viewer.md) | GET | Retrieves the authenticated viewer from Universe. |
| [List User External Emails](actions/list-user-external-emails.md) | GET | Retrieves external email addresses for a Universe user. |

### Userprofile

| Action | Method | Description |
| --- | --- | --- |
| [Get Profile](actions/get-profile.md) | GET | Retrieves a specific profile from Universe. |

