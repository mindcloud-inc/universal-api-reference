# <img src="https://images.mindcloud.co/apps/icons/unisender-icon-180_1775673512434.png" alt="Unisender logo" width="28" height="28"> Unisender: Universal API

Unisender is an email, SMS, contact-list, and subscriber management platform for bulk messaging, subscriber data, templates, campaigns, and delivery statistics through the Unisender API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/unisender/latest
- **Category:** Marketing
- **Actions:** 32
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.unisender.com/
- **Vendor API docs:** https://www.unisender.com/ru/support/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Lists](actions/list-lists.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unisender/latest/actions/list-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (32)

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign Common Stats](actions/get-campaign-common-stats.md) | GET | Retrieves campaign summary stats from Unisender. |
| [Get Campaign Delivery Stats](actions/get-campaign-delivery-stats.md) | GET | Retrieves campaign delivery stats from Unisender. |
| [Get Campaign Status](actions/get-campaign-status.md) | GET | Retrieves a campaign status from Unisender. |
| [Get Campaigns](actions/get-campaigns.md) | GET | Retrieves campaigns from Unisender. |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact Field Values](actions/get-contact-field-values.md) | GET | Retrieves contact field values from Unisender. |
| [Get Fields](actions/get-fields.md) | GET | Retrieves custom fields from Unisender. |

### Custom Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Sender Domain List](actions/get-sender-domain-list.md) | GET | Retrieves sender domain details from Unisender. |

### Email Templates

| Action | Method | Description |
| --- | --- | --- |
| [Get Template](actions/get-template.md) | GET | Retrieves a template from Unisender. |
| [Get Templates](actions/get-templates.md) | GET | Retrieves templates from Unisender. |
| [List Templates](actions/list-templates.md) | GET | Retrieves templates from Unisender. |

### Emails

| Action | Method | Description |
| --- | --- | --- |
| [Check Email](actions/check-email.md) | GET | Retrieves email validation results from Unisender. |

### Export Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Export Contacts](actions/export-contacts.md) | GET | Exports contacts from Unisender as an asynchronous job. |

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [Create List](actions/create-list.md) | POST | Creates a new list in Unisender. |
| [Delete List](actions/delete-list.md) | DELETE | Deletes an existing list from Unisender. |
| [List Lists](actions/list-lists.md) | GET | Retrieves lists from Unisender. |
| [Update List](actions/update-list.md) | PUT | Updates an existing list in Unisender. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Check SMS](actions/check-sms.md) | GET | Retrieves SMS validation results from Unisender. |
| [Get Actual Message Version](actions/get-actual-message-version.md) | GET | Retrieves the current message version from Unisender. |
| [Get Message](actions/get-message.md) | GET | Retrieves a message from Unisender. |
| [Get Messages](actions/get-messages.md) | GET | Retrieves messages from Unisender. |
| [Get Web Version](actions/get-web-version.md) | GET | Retrieves a message web version from Unisender. |
| [List Messages](actions/list-messages.md) | GET | Retrieves messages from Unisender. |

### Notes

| Action | Method | Description |
| --- | --- | --- |
| [Get Subscriber Note](actions/get-subscriber-note.md) | GET | Retrieves a subscriber note from Unisender. |
| [Get Subscriber Notes](actions/get-subscriber-notes.md) | GET | Retrieves subscriber notes from Unisender. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Visited Links](actions/get-visited-links.md) | GET | Retrieves visited links from Unisender. |

### Subscribers

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Unisender. |
| [Get Contact Count](actions/get-contact-count.md) | GET | Retrieves a filtered contact count from Unisender. |
| [Get Total Contacts Count](actions/get-total-contacts-count.md) | GET | Retrieves the total contact count from Unisender. |
| [Is Contact In Lists](actions/is-contact-in-lists.md) | GET | Finds whether a contact is in Unisender lists. |
| [Subscribe Contact](actions/subscribe-contact.md) | POST | Creates a subscribed contact in Unisender. |
| [Unsubscribe Contact](actions/unsubscribe-contact.md) | PUT | Updates a contact subscription in Unisender. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Get Tags](actions/get-tags.md) | GET | Retrieves tags from Unisender. |

