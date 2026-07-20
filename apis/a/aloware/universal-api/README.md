# <img src="https://images.mindcloud.co/apps/icons/aloware-logo-only-svg-1_1773759250798.png" alt="Aloware logo" width="28" height="28"> Aloware: Universal API

Manage leads, send messages, run calls, and automate dialing

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/aloware/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.aloware.com
- **Vendor API docs:** https://support.aloware.com/en/collections/8591828-webhooks

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aloware/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Call

| Action | Method | Description |
| --- | --- | --- |
| [Establish Two-Legged Call](actions/establish-two-legged-call.md) | POST | Establishes a two-legged call in Aloware. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Aloware. |
| [Disenroll Contact From Sequences](actions/disenroll-contact-from-sequences.md) | PUT | Disenrolls a contact from Aloware sequences. |
| [Enroll Contact In Sequence](actions/enroll-contact-in-sequence.md) | PUT | Enrolls a contact in an Aloware sequence. |
| [Lookup Contact By Phone Number](actions/lookup-contact-by-phone-number.md) | GET | Finds a contact in Aloware by phone number. |
| [Remove Contact From Power Dialer Lists](actions/remove-contact-from-power-dialer-lists.md) | PUT | Removes a contact from Aloware power dialer lists. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Aloware. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Send SMS](actions/send-sms.md) | POST | Sends an SMS or MMS message from Aloware. |

### Power Dialer List

| Action | Method | Description |
| --- | --- | --- |
| [Clear Power Dialer List](actions/clear-power-dialer-list.md) | DELETE | Clears all contacts from an Aloware power dialer list. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Clear User Power Dialer Lists](actions/clear-user-power-dialer-lists.md) | PUT | Clears all contacts from an Aloware user's power dialer lists. |
| [List Users](actions/list-users.md) | GET | Retrieves user records from your Aloware account. |

