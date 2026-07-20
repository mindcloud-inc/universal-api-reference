# <img src="https://images.mindcloud.co/apps/icons/channels_1776860666505.png" alt="Channels logo" width="28" height="28"> Channels: Universal API

Channels is a business phone system and call center platform for managing users, contacts, phone numbers, calls, recordings, finance data, reports, and related phone operations through the Channels REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/channels/latest
- **Category:** Support / Contact Center
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.channels.app/
- **Vendor API docs:** https://developers.channels.app/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/channels/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Activities

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact History](actions/get-contact-history.md) | GET | Retrieves contact history from Channels. |

### Calls

| Action | Method | Description |
| --- | --- | --- |
| [Get Call](actions/get-call.md) | GET | Retrieves a call from Channels. |
| [List Calls](actions/list-calls.md) | GET | Retrieves calls from Channels. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Add Or Update Contact Details](actions/add-or-update-contact-details.md) | PUT | Updates contact details in Channels, or creates them if missing. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from Channels. |
| [Edit Contact Details](actions/edit-contact-details.md) | PUT | Updates existing contact details in Channels. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Channels. |
| [Get Contact Details](actions/get-contact-details.md) | GET | Retrieves contact details from Channels. |
| [Import Contact](actions/import-contact.md) | POST | Imports a contact into Channels. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Channels. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Channels. |

### Notes

| Action | Method | Description |
| --- | --- | --- |
| [Add Contact Note](actions/add-contact-note.md) | POST | Creates a contact note in Channels. |

### Phone Numbers

| Action | Method | Description |
| --- | --- | --- |
| [Add Contact Alternative MSISDN](actions/add-contact-alternative-msisdn.md) | POST | Creates an alternative contact phone number in Channels. |
| [Block MSISDN](actions/block-msisdn.md) | POST | Blocks a phone number in Channels. |
| [Delete Contact Alternative MSISDN](actions/delete-contact-alternative-msisdn.md) | DELETE | Deletes an alternative contact phone number from Channels. |
| [Get Number Do Not Call History](actions/get-number-do-not-call-history.md) | GET | Retrieves do-not-call history for a phone number in Channels. |
| [List Contact Alternative MSISDNs](actions/list-contact-alternative-msisd-ns.md) | GET | Retrieves alternative contact phone numbers from Channels. |
| [List Do Not Call History](actions/list-do-not-call-history.md) | GET | Retrieves do-not-call history from Channels. |
| [List Phone Numbers](actions/list-phone-numbers.md) | GET | Retrieves phone numbers from Channels. |
| [Set Inbound Call Forwarding](actions/set-inbound-call-forwarding.md) | PUT | Updates inbound call forwarding for a phone number in Channels. |
| [Unblock MSISDN](actions/unblock-msisdn.md) | DELETE | Unblocks a phone number in Channels. |

### Recordings

| Action | Method | Description |
| --- | --- | --- |
| [Create Public Recording Link](actions/create-public-recording-link.md) | POST | Creates a public recording link in Channels. |
| [Create Recordings Archive Link](actions/create-recordings-archive-link.md) | POST | Creates a recordings archive link in Channels. |
| [Delete Public Recording Link](actions/delete-public-recording-link.md) | DELETE | Deletes a public recording link from Channels. |
| [List Public Recording Links](actions/list-public-recording-links.md) | GET | Retrieves public recording links from Channels. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get User Stats](actions/get-user-stats.md) | GET | Retrieves account user statistics from Channels. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Check User Exists](actions/check-user-exists.md) | GET | Finds whether a user exists in Channels by email address. |
| [Disable User](actions/disable-user.md) | PUT | Disables a user in Channels. |
| [Enable User](actions/enable-user.md) | PUT | Enables a user in Channels. |
| [List Users](actions/list-users.md) | GET | Retrieves users from Channels. |

