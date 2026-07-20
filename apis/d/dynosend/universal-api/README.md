# <img src="https://images.mindcloud.co/apps/icons/dynosend_1776113832853.png" alt="Dynosend logo" width="28" height="28"> Dynosend: Universal API

Create campaigns, manage contacts, and send transactional messages

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dynosend/latest
- **Category:** Marketing
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://dynosend.com
- **Vendor API docs:** https://developers.dynosend.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check Blacklist](actions/check-blacklist.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dynosend/latest/actions/check-blacklist?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Audience

| Action | Method | Description |
| --- | --- | --- |
| [Get Audience](actions/get-audience.md) | GET | Retrieves an audience from Dynosend. |
| [List Audiences](actions/list-audiences.md) | GET | Retrieves audiences from Dynosend. |

### Blacklist Contact

| Action | Method | Description |
| --- | --- | --- |
| [Add to Blacklist](actions/add-to-blacklist.md) | PUT | Adds a contact to the Dynosend blacklist. |
| [Check Blacklist](actions/check-blacklist.md) | GET | Checks whether a contact is blacklisted in Dynosend. |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign](actions/get-campaign.md) | GET | Retrieves a campaign from Dynosend. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaigns from Dynosend. |
| [Pause Campaign](actions/pause-campaign.md) | PUT | Pauses a campaign in Dynosend. |
| [Resume Campaign](actions/resume-campaign.md) | PUT | Resumes a campaign in Dynosend. |
| [Start Campaign](actions/start-campaign.md) | PUT | Starts a campaign in Dynosend. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Add Contact Tags by Email](actions/add-contact-tags-by-email.md) | PUT | Adds tags to a Dynosend contact by email address. |
| [Add Contact Tags by UID](actions/add-contact-tags-by-uid.md) | PUT | Adds tags to a Dynosend contact by UID. |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Dynosend. |
| [Create Contact and Ignore Double Opt-In](actions/create-contact-ignore-double-opt-in.md) | POST | Creates a new contact in Dynosend without double opt-in. |
| [Delete Contact by Email](actions/delete-contact-by-email.md) | DELETE | Deletes a Dynosend contact by email address. |
| [Delete Contact by UID](actions/delete-contact-by-uid.md) | DELETE | Deletes a Dynosend contact by UID. |
| [Find Duplicate Contacts by Email](actions/find-duplicate-contacts-by-email.md) | GET | Finds duplicate contacts in Dynosend by email address. |
| [Get Contact by Email](actions/get-contact-by-email.md) | GET | Retrieves a contact from Dynosend by email address. |
| [Get Contact by UID](actions/get-contact-by-uid.md) | GET | Retrieves a contact from Dynosend by UID. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Dynosend. |
| [Subscribe Contact by Email](actions/subscribe-contact-by-email.md) | PUT | Subscribes a Dynosend contact by email address. |
| [Subscribe Contact by UID](actions/subscribe-contact-by-uid.md) | PUT | Subscribes a Dynosend contact by UID. |
| [Unsubscribe Contact by Email](actions/unsubscribe-contact-by-email.md) | PUT | Unsubscribes a Dynosend contact by email address. |
| [Unsubscribe Contact by UID](actions/unsubscribe-contact-by-uid.md) | PUT | Unsubscribes a Dynosend contact by UID. |
| [Update Contact by Email](actions/update-contact-by-email.md) | PUT | Updates a contact in Dynosend by email address. |
| [Update Contact by UID](actions/update-contact-by-uid.md) | PUT | Updates a contact in Dynosend by UID. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Send Contact Event by Email](actions/send-contact-event-by-email.md) | POST | Creates an event in Dynosend for an email address. |
| [Send Contact Event by UID](actions/send-contact-event-by-uid.md) | POST | Creates an event in Dynosend for a contact UID. |

### Push Device

| Action | Method | Description |
| --- | --- | --- |
| [Register Push Device by Contact UID](actions/register-push-device-by-contact-uid.md) | POST | Registers a push device in Dynosend by contact UID. |
| [Register Push Device by Email](actions/register-push-device-by-email.md) | POST | Registers a push device in Dynosend by email address. |

### Transactional Message

| Action | Method | Description |
| --- | --- | --- |
| [Send Transactional Message](actions/send-transactional-message.md) | POST | Creates a transactional message in Dynosend. |
| [Send Transactional Message with External Content](actions/send-transactional-message-with-external-content.md) | POST | Creates a transactional message in Dynosend with external content. |

