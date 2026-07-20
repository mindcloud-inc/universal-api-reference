# <img src="https://images.mindcloud.co/apps/icons/whatsscale-icon_1776698839496.png" alt="WhatsScale logo" width="28" height="28"> WhatsScale: Universal API

WhatsScale automates WhatsApp messaging, sessions, contacts, stories, phone validation, and CRM contact management through the WhatsScale REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/whatsScale/latest
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://whatsscale.com
- **Vendor API docs:** https://whatsscale.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Test Authentication](actions/test-authentication.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whatsScale/latest/actions/test-authentication?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Authentication

| Action | Method | Description |
| --- | --- | --- |
| [Test Authentication](actions/test-authentication.md) | GET | Retrieves your authentication details from WhatsScale. |

### Crm Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create CRM Contact](actions/create-crm-contact.md) | POST | Creates a CRM contact in WhatsScale. |
| [Delete CRM Contact](actions/delete-crm-contact.md) | DELETE | Deletes an existing CRM contact from WhatsScale. |
| [Find CRM Contact by Phone](actions/find-crm-contact-by-phone.md) | GET | Finds a CRM contact in WhatsScale by phone number. |
| [Get CRM Contact](actions/get-crm-contact.md) | GET | Retrieves a CRM contact from WhatsScale. |
| [List CRM Contacts](actions/list-crm-contacts.md) | GET | Retrieves CRM contacts from your WhatsScale account. |
| [Update CRM Contact](actions/update-crm-contact.md) | PUT | Updates an existing CRM contact in WhatsScale. |

### Crm Contact Tag

| Action | Method | Description |
| --- | --- | --- |
| [Add Tag to CRM Contact](actions/add-tag-to-crm-contact.md) | PUT | Adds a tag to an existing WhatsScale CRM contact. |
| [Remove Tag from CRM Contact](actions/remove-tag-from-crm-contact.md) | PUT | Removes a tag from an existing WhatsScale CRM contact. |

### Crm Tag

| Action | Method | Description |
| --- | --- | --- |
| [List CRM Tags](actions/list-crm-tags.md) | GET | Retrieves CRM tags from your WhatsScale account. |

### Document Send Job

| Action | Method | Description |
| --- | --- | --- |
| [Send Document](actions/send-document.md) | POST | Creates a document send job in WhatsScale. |

### Image Message

| Action | Method | Description |
| --- | --- | --- |
| [Send Image](actions/send-image.md) | POST | Sends an image message through WhatsScale. |

### Image Story Job

| Action | Method | Description |
| --- | --- | --- |
| [Post Image Story](actions/post-image-story.md) | POST | Creates an image story job in WhatsScale. |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Check Job Status](actions/check-job-status.md) | GET | Retrieves an async job status from WhatsScale. |

### Location Message

| Action | Method | Description |
| --- | --- | --- |
| [Send Location](actions/send-location.md) | POST | Sends a location message through WhatsScale. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Send Text Message](actions/send-text-message.md) | POST | Sends a text message through WhatsScale. |

### Poll Message

| Action | Method | Description |
| --- | --- | --- |
| [Send Poll](actions/send-poll.md) | POST | Sends a poll message through WhatsScale. |

### Session

| Action | Method | Description |
| --- | --- | --- |
| [List Sessions](actions/list-sessions.md) | GET | Retrieves WhatsApp sessions linked to your WhatsScale account. |

### Text Story Job

| Action | Method | Description |
| --- | --- | --- |
| [Post Text Story](actions/post-text-story.md) | POST | Creates a text story job in WhatsScale. |

### Video Send Job

| Action | Method | Description |
| --- | --- | --- |
| [Send Video](actions/send-video.md) | POST | Creates a video send job in WhatsScale. |

### Video Story Job

| Action | Method | Description |
| --- | --- | --- |
| [Post Video Story](actions/post-video-story.md) | POST | Creates a video story job in WhatsScale. |

### Whatsapp Contact

| Action | Method | Description |
| --- | --- | --- |
| [List WhatsApp Contacts](actions/list-whats-app-contacts.md) | GET | Retrieves WhatsApp contacts from a WhatsScale session. |

### Whatsapp Group

| Action | Method | Description |
| --- | --- | --- |
| [List WhatsApp Groups](actions/list-whats-app-groups.md) | GET | Retrieves WhatsApp groups from a WhatsScale session. |

### Whatsapp Number Check

| Action | Method | Description |
| --- | --- | --- |
| [Check WhatsApp Number](actions/check-whats-app-number.md) | GET | Checks whether a phone number uses WhatsApp via WhatsScale. |

