# <img src="https://images.mindcloud.co/apps/icons/swipe-one_1774288224822.png" alt="Swipe One logo" width="28" height="28"> Swipe One: Universal API

Manage contacts, automate marketing, and track sales pipelines

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/swipeOne/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 36
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.swipeone.com
- **Vendor API docs:** https://docs.swipeone.com/en/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Contact Fields](actions/get-contact-fields.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/swipeOne/latest/actions/get-contact-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (36)

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Zapier Contact](actions/create-zapier-contact.md) | POST |  |

### Contact Field

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact Fields](actions/get-contact-fields.md) | GET |  |

### Contact Property

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact Property](actions/create-contact-property.md) | POST |  |
| [Get Contact Property](actions/get-contact-property.md) | GET |  |
| [List Contact Properties](actions/list-contact-properties.md) | GET |  |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST |  |
| [Get Contact](actions/get-contact.md) | GET |  |
| [List Contacts](actions/list-contacts.md) | GET |  |
| [List Segment Contacts](actions/list-segment-contacts.md) | GET |  |
| [List Tag Contacts](actions/list-tag-contacts.md) | GET |  |
| [Search Contacts](actions/search-contacts.md) | GET |  |
| [Update Contact Tags](actions/update-contact-tags.md) | PUT |  |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Create Zapier Event](actions/create-zapier-event.md) | POST |  |
| [List Make Events](actions/list-make-events.md) | GET |  |
| [List Zapier Events](actions/list-zapier-events.md) | GET |  |

### Event Definition

| Action | Method | Description |
| --- | --- | --- |
| [Create Event Definition](actions/create-event-definition.md) | POST |  |

### Event Property

| Action | Method | Description |
| --- | --- | --- |
| [Get Make Event Properties](actions/get-make-event-properties.md) | GET |  |
| [Get Zapier Event Properties](actions/get-zapier-event-properties.md) | GET |  |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Create Event](actions/create-event.md) | POST |  |
| [List Contact Events](actions/list-contact-events.md) | GET |  |

### Note

| Action | Method | Description |
| --- | --- | --- |
| [Create Note](actions/create-note.md) | POST |  |
| [Get Note](actions/get-note.md) | GET |  |
| [List Contact Notes](actions/list-contact-notes.md) | GET |  |
| [List Notes](actions/list-notes.md) | GET |  |
| [Update Note](actions/update-note.md) | PUT |  |

### Segments

| Action | Method | Description |
| --- | --- | --- |
| [Create Segment](actions/create-segment.md) | POST |  |
| [Get Segment](actions/get-segment.md) | GET |  |
| [List Segments](actions/list-segments.md) | GET |  |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST |  |
| [Get Tag](actions/get-tag.md) | GET |  |
| [List Tags](actions/list-tags.md) | GET |  |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST |  |
| [Get Task](actions/get-task.md) | GET |  |
| [List Contact Tasks](actions/list-contact-tasks.md) | GET |  |
| [List Tasks](actions/list-tasks.md) | GET |  |
| [Update Task](actions/update-task.md) | PUT |  |

