# <img src="https://images.mindcloud.co/apps/icons/just-call_1774555230128.png" alt="JustCall logo" width="28" height="28"> JustCall: Universal API

Manage calls, texts, contacts, and phone numbers

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/justCall/latest
- **Category:** Support / Contact Center
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://justcall.io
- **Vendor API docs:** https://developer.justcall.io/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List All Users](actions/list-all-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/justCall/latest/actions/list-all-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Call

| Action | Method | Description |
| --- | --- | --- |
| [Download Call Recording](actions/download-call-recording.md) | GET | Downloads a call recording from JustCall. |
| [Get a Call](actions/get-a-call.md) | GET | Retrieves a call from JustCall. |
| [Get Call Journey](actions/get-call-journey.md) | GET | Retrieves a call journey from JustCall. |
| [List All Calls](actions/list-all-calls.md) | GET | Retrieves calls from JustCall. |
| [Update a Call](actions/update-a-call.md) | PUT | Updates an existing call in JustCall. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Add Contacts to Blacklist](actions/bulk-add-contacts-to-blacklist.md) | POST | Adds contacts to the JustCall blacklist. |
| [Create Contact](actions/create-contact.md) | POST | Creates a contact in JustCall. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from JustCall. |
| [Get a Contact](actions/get-a-contact.md) | GET | Retrieves a contact from JustCall. |
| [List All Contacts](actions/list-all-contacts.md) | GET | Retrieves contacts from JustCall. |
| [List Blacklisted Contacts](actions/list-blacklisted-contacts.md) | GET | Retrieves blacklisted contacts from JustCall. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in JustCall. |
| [Update Contact Status](actions/update-contact-status.md) | PUT | Updates contact status in JustCall. |

### Phone Number

| Action | Method | Description |
| --- | --- | --- |
| [Get a Phone Number](actions/get-a-phone-number.md) | GET | Retrieves a phone number from JustCall. |
| [List All Phone Numbers](actions/list-all-phone-numbers.md) | GET | Retrieves phone numbers from JustCall. |

### Text

| Action | Method | Description |
| --- | --- | --- |
| [Check Reply](actions/check-reply.md) | GET | Checks for a reply in JustCall. |
| [Get a Text](actions/get-a-text.md) | GET | Retrieves a text from JustCall. |
| [List All Texts](actions/list-all-texts.md) | GET | Retrieves texts from JustCall. |
| [Send SMS/MMS](actions/send-sms-mms.md) | POST | Creates an SMS or MMS message in JustCall. |

### Thread

| Action | Method | Description |
| --- | --- | --- |
| [Get a Thread](actions/get-a-thread.md) | GET | Retrieves a text thread from JustCall. |
| [List All Threads](actions/list-all-threads.md) | GET | Retrieves text threads from JustCall. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get a User](actions/get-a-user.md) | GET | Retrieves a user from JustCall. |
| [List All Users](actions/list-all-users.md) | GET | Retrieves users from JustCall. |
| [Update User Availability](actions/update-user-availability.md) | PUT | Updates user availability in JustCall. |

