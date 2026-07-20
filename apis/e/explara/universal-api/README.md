# <img src="https://images.mindcloud.co/apps/icons/explara_1775253299857.png" alt="Explara logo" width="28" height="28"> Explara: Universal API

Explara is an all-in-one platform for creators and small businesses to sell event tickets, memberships, digital products, and raise funds.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/explara/latest
- **Category:** Marketing / Events & Webinars
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.explara.com
- **Vendor API docs:** https://apidocs.explara.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Account Profile](actions/account-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/explara/latest/actions/account-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Attendee

| Action | Method | Description |
| --- | --- | --- |
| [Attendee Form](actions/attendee-form.md) | GET | Retrieves an attendee form from Explara. |
| [List Event Attendees](actions/list-event-attendees.md) | GET | Retrieves event attendees from Explara. |

### Cart

| Action | Method | Description |
| --- | --- | --- |
| [Event Cart Calculation](actions/event-cart-calculation.md) | GET | Retrieves an event cart calculation from Explara. |
| [Membership Generate Cart](actions/membership-generate-cart.md) | GET | Retrieves a membership cart calculation from Explara. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Event Details](actions/get-event-details.md) | GET | Retrieves event details from Explara. |
| [List Events](actions/list-events.md) | GET | Retrieves events from Explara. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [List Groups](actions/list-groups.md) | GET | Retrieves groups from Explara. |

### Member

| Action | Method | Description |
| --- | --- | --- |
| [Group Members](actions/group-members.md) | GET | Retrieves group members from Explara. |
| [Member Profile](actions/member-profile.md) | GET | Retrieves a member profile from Explara. |
| [Search Group Members](actions/search-group-members.md) | GET | Finds group members in Explara by keyword or email. |

### Membership

| Action | Method | Description |
| --- | --- | --- |
| [Edit Member Form](actions/edit-member-form.md) | GET | Retrieves an edit member form from Explara. |
| [Membership Form](actions/membership-form.md) | GET | Retrieves a membership form from Explara. |
| [Membership Members Details](actions/membership-members-details.md) | GET | Retrieves membership member details from Explara. |
| [Membership Order Details](actions/membership-order-details.md) | GET | Retrieves membership order details from Explara. |
| [My Membership](actions/my-membership.md) | GET | Retrieves your memberships from Explara. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Event Generate Order](actions/event-generate-order.md) | POST | Creates a new event order in Explara. |
| [Order Details](actions/order-details.md) | GET | Retrieves order details from Explara. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Event Report](actions/get-event-report.md) | GET | Retrieves an event report from Explara. |

### Ticket

| Action | Method | Description |
| --- | --- | --- |
| [List Tickets](actions/list-tickets.md) | GET | Retrieves tickets from Explara. |

### User Profile

| Action | Method | Description |
| --- | --- | --- |
| [Account Profile](actions/account-profile.md) | GET | Retrieves an account profile from Explara. |

