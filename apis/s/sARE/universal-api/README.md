# <img src="https://images.mindcloud.co/apps/icons/favicon-21_1775595231180.png" alt="SARE logo" width="28" height="28"> SARE: Universal API

SARE is a marketing and communications platform for contact lists, groups, newsletters, mailings, transactional email, and SMS messaging.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sARE/latest
- **Category:** Marketing
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://sare.pl/
- **Vendor API docs:** https://dev.sare.pl/rest-api/other/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Available Group Numbers](actions/list-available-group-numbers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sARE/latest/actions/list-available-group-numbers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Add Subscribers](actions/add-subscribers.md) | POST | Creates new subscribers in SARE. |
| [Delete Subscribers](actions/delete-subscribers.md) | DELETE | Deletes subscribers from SARE. |
| [Get Subscriber By Email Hash](actions/get-subscriber-by-email-hash.md) | GET | Retrieves a subscriber from SARE by email hash. |
| [Get Subscriber Status By Email Hash](actions/get-subscriber-status-by-email-hash.md) | GET | Retrieves subscriber status from SARE by email hash. |
| [Get Subscriber Statuses By Email List](actions/get-subscriber-statuses-by-email-list.md) | GET | Retrieves subscriber statuses from SARE by email address list. |
| [Get Subscribers By Email List](actions/get-subscribers-by-email-list.md) | GET | Retrieves subscribers from SARE by email address list. |
| [List Email Properties](actions/list-email-properties.md) | GET | Lists available subscriber properties in SARE. |
| [List Group Emails](actions/list-group-emails.md) | GET | Retrieves subscriber email addresses from a SARE group. |
| [Update Subscribers](actions/update-subscribers.md) | PUT | Updates existing subscribers in SARE. |

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [Add Subscribers To Groups By Email Address](actions/add-subscribers-to-groups-by-email-address.md) | PUT | Adds subscribers to SARE groups by email address. |
| [Clear Group](actions/clear-group.md) | PUT | Removes all email addresses from a SARE group. |
| [Create Group](actions/create-group.md) | POST | Creates a new group in SARE. |
| [Delete Group](actions/delete-group.md) | DELETE | Deletes an existing group from SARE. |
| [Get Group](actions/get-group.md) | GET | Retrieves a specific group from SARE. |
| [List Available Group Numbers](actions/list-available-group-numbers.md) | GET | Lists available group numbers in SARE. |
| [List Groups](actions/list-groups.md) | GET | Lists groups in SARE. |
| [Remove Subscribers From Groups By Email Address](actions/remove-subscribers-from-groups-by-email-address.md) | PUT | Removes subscribers from SARE groups by email address. |
| [Update Group](actions/update-group.md) | PUT | Updates an existing group in SARE. |

