# <img src="https://images.mindcloud.co/apps/icons/mask-group-1_1781897432956.png" alt="Growby logo" width="28" height="28"> Growby: Universal API

Growby provides WhatsApp Business API access and marketing automation for managing contacts, groups, and message delivery.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/growby/latest
- **Category:** Marketing
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.growby.net
- **Vendor API docs:** https://www.postman.com/growby-documentation/growby-api/documentation/i4ul9w0/growby-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Contacts](actions/list-contacts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/growby/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Growby. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from Growby. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Growby. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Growby. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Add Contact To Group By Group ID](actions/add-contact-to-group-by-group-id.md) | POST | Adds a contact to a Growby group by group ID. |
| [Add Contact To Group By Group Name](actions/add-contact-to-group-by-group-name.md) | POST | Adds a contact to a Growby group by group name. |
| [Bulk Add Contacts To Group By Group ID](actions/bulk-add-contacts-to-group-by-group-id.md) | POST | Adds multiple contacts to a Growby group by group ID. |
| [Bulk Add Contacts To Group By Group Name](actions/bulk-add-contacts-to-group-by-group-name.md) | POST | Adds multiple contacts to a Growby group by group name. |
| [Create Group](actions/create-group.md) | POST | Creates a new group in Growby. |
| [List Groups](actions/list-groups.md) | GET | Retrieves groups from Growby. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Send Carousel Template Message](actions/send-carousel-template-message.md) | POST | Sends a carousel template message through Growby. |
| [Send Document Message](actions/send-document-message.md) | POST | Sends a document message through Growby. |
| [Send Image Reply Message](actions/send-image-reply-message.md) | POST | Sends an image reply message through Growby. |
| [Send Interactive Template Message](actions/send-interactive-template-message.md) | POST | Sends an interactive template message through Growby. |
| [Send Media Message](actions/send-media-message.md) | POST | Sends a media message through Growby. |
| [Send Media Template Message](actions/send-media-template-message.md) | POST | Sends a media template message through Growby. |
| [Send Media Template Message With Parameters](actions/send-media-template-message-with-parameters.md) | POST | Sends a parameterized media template message through Growby. |
| [Send Message V2](actions/send-message-v2.md) | POST | Sends a message through Growby v2. |
| [Send Template Message](actions/send-template-message.md) | POST | Sends a template message through Growby. |
| [Send Template Message With Parameters](actions/send-template-message-with-parameters.md) | POST | Sends a parameterized template message through Growby. |
| [Send Text Message](actions/send-text-message.md) | POST | Sends a text message through Growby. |
| [Send Text Reply Message](actions/send-text-reply-message.md) | POST | Sends a text reply message through Growby. |
| [Send Text Template Message](actions/send-text-template-message.md) | POST | Sends a text template message through Growby. |
| [Send Video Message](actions/send-video-message.md) | POST | Sends a video message through Growby. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [List Message Templates](actions/list-message-templates.md) | GET | Retrieves message templates from Growby. |

