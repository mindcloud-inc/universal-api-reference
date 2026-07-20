# <img src="https://images.mindcloud.co/apps/icons/respondio_1773263222190.png" alt="respond.io logo" width="28" height="28"> respond.io: Universal API

Manage respond.io conversations, contacts, channels, messages, and workspace users

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/respondio/latest
- **Category:** Communication / Team Messaging
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://respond.io/
- **Vendor API docs:** https://developers.respond.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Contact](actions/get-contact.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/respondio/latest/actions/get-contact?connectionId=$CONNECTION_ID&identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Channel

| Action | Method | Description |
| --- | --- | --- |
| [List Channels](actions/list-channels.md) | GET | Retrieves channels from respond.io. |
| [List Contact Channels](actions/list-contact-channels.md) | GET | Retrieves contact channels from respond.io. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in respond.io. |
| [Create Or Update Contact](actions/create-or-update-contact.md) | PUT | Finds a contact in respond.io, or creates one if no match is found. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes a contact from respond.io. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from respond.io. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from respond.io. |
| [Merge Contacts](actions/merge-contacts.md) | PUT | Merges two contacts in respond.io. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in respond.io. |
| [Update Contact Lifecycle](actions/update-contact-lifecycle.md) | PUT | Updates a contact lifecycle in respond.io. |

### Conversation

| Action | Method | Description |
| --- | --- | --- |
| [Assign Or Unassign Conversation](actions/assign-or-unassign-conversation.md) | PUT | Updates a conversation assignee in respond.io. |
| [Open Or Close Conversation](actions/open-or-close-conversation.md) | PUT | Updates a conversation status in respond.io. |

### Customfield

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom Field](actions/create-custom-field.md) | POST | Creates a new custom field in respond.io. |
| [Get Custom Field](actions/get-custom-field.md) | GET | Retrieves a custom field from respond.io. |
| [List Custom Fields](actions/list-custom-fields.md) | GET | Retrieves custom fields from respond.io. |

### Note

| Action | Method | Description |
| --- | --- | --- |
| [List Closing Notes](actions/list-closing-notes.md) | GET | Retrieves closing notes from respond.io. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Add Tags](actions/add-tags.md) | POST | Adds tags to a contact in respond.io. |
| [Create Space Tag](actions/create-space-tag.md) | POST | Creates a new space tag in respond.io. |
| [Delete Space Tag](actions/delete-space-tag.md) | DELETE | Deletes a space tag from respond.io. |
| [Delete Tags](actions/delete-tags.md) | DELETE | Deletes tags from a contact in respond.io. |
| [Update Space Tag](actions/update-space-tag.md) | PUT | Updates an existing space tag in respond.io. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [List Message Templates](actions/list-message-templates.md) | GET | Retrieves message templates from respond.io. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves a user from respond.io. |
| [List Users](actions/list-users.md) | GET | Retrieves users from respond.io. |

