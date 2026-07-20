# <img src="https://images.mindcloud.co/apps/icons/marketing-master-io_1777060421589.png" alt="Marketing Master IO logo" width="28" height="28"> Marketing Master IO: Universal API

Manage contacts, subscribers, chatbots, and Facebook pages

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/marketingMasterIO/latest
- **Category:** Marketing
- **Actions:** 37
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://marketingmaster.io/
- **Vendor API docs:** https://developers.marketingmaster.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Validate Access Token](actions/validate-access-token.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/marketingMasterIO/latest/actions/validate-access-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (37)

### Access Token

| Action | Method | Description |
| --- | --- | --- |
| [Validate Access Token](actions/validate-access-token.md) | GET | Validates an access token in Marketing Master IO. |

### Chat Sequence

| Action | Method | Description |
| --- | --- | --- |
| [Get Chat Sequence](actions/get-chat-sequence.md) | GET | Retrieves a chat sequence from Marketing Master IO. |
| [List Chat Sequences](actions/list-chat-sequences.md) | GET | Retrieves chat sequences from Marketing Master IO. |

### Chat Sequence Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Opt In Chat Sequence Subscriber](actions/opt-in-chat-sequence-subscriber.md) | PUT | Opts a subscriber into a chat sequence in Marketing Master IO. |
| [Opt Out Chat Sequence Subscriber](actions/opt-out-chat-sequence-subscriber.md) | PUT | Removes a subscriber from a chat sequence in Marketing Master IO. |

### Chatbot Flow

| Action | Method | Description |
| --- | --- | --- |
| [Get Chatbot Flow](actions/get-chatbot-flow.md) | GET | Retrieves a chatbot flow from Marketing Master IO. |
| [List Chatbot Flows](actions/list-chatbot-flows.md) | GET | Retrieves chatbot flows from Marketing Master IO. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Marketing Master IO. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from Marketing Master IO. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Marketing Master IO. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Marketing Master IO. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Marketing Master IO. |

### Contact Book

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact Book](actions/create-contact-book.md) | POST | Creates a new contact book in Marketing Master IO. |
| [Delete Contact Book](actions/delete-contact-book.md) | DELETE | Deletes an existing contact book from Marketing Master IO. |
| [Get Contact Book](actions/get-contact-book.md) | GET | Retrieves a contact book from Marketing Master IO. |
| [List Contact Books](actions/list-contact-books.md) | GET | Retrieves contact books from Marketing Master IO. |
| [Update Contact Book](actions/update-contact-book.md) | PUT | Updates an existing contact book in Marketing Master IO. |

### Contact Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact Tag](actions/create-contact-tag.md) | POST | Creates a new contact tag in Marketing Master IO. |
| [Delete Contact Tag](actions/delete-contact-tag.md) | DELETE | Deletes an existing contact tag from Marketing Master IO. |
| [Get Contact Tag](actions/get-contact-tag.md) | GET | Retrieves a contact tag from Marketing Master IO. |
| [List Contact Tags](actions/list-contact-tags.md) | GET | Retrieves contact tags from Marketing Master IO. |

### Custom Variable

| Action | Method | Description |
| --- | --- | --- |
| [Get Custom Variable](actions/get-custom-variable.md) | GET | Retrieves a custom variable from Marketing Master IO. |
| [List Custom Variables](actions/list-custom-variables.md) | GET | Retrieves custom variables from Marketing Master IO. |

### Facebook Page

| Action | Method | Description |
| --- | --- | --- |
| [Disable Facebook Page](actions/disable-facebook-page.md) | PUT | Disables an imported Facebook page in Marketing Master IO. |
| [Enable Facebook Page](actions/enable-facebook-page.md) | PUT | Enables an imported Facebook page in Marketing Master IO. |
| [Get Facebook Page](actions/get-facebook-page.md) | GET | Retrieves an imported Facebook page from Marketing Master IO. |
| [List Facebook Pages](actions/list-facebook-pages.md) | GET | Retrieves imported Facebook pages from Marketing Master IO. |

### Google Sheet

| Action | Method | Description |
| --- | --- | --- |
| [Get Google Sheet](actions/get-google-sheet.md) | GET | Retrieves a Google Sheet from Marketing Master IO. |
| [List Google Sheets](actions/list-google-sheets.md) | GET | Retrieves imported Google Sheets from Marketing Master IO. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Send Custom Message](actions/send-custom-message.md) | POST | Sends a custom message to a subscriber in Marketing Master IO. |
| [Send Flow Message](actions/send-flow-message.md) | POST | Sends a flow message to a subscriber in Marketing Master IO. |

### Messenger Subscriber

| Action | Method | Description |
| --- | --- | --- |
| [Add Subscriber Tag](actions/add-subscriber-tag.md) | PUT | Adds a tag to a Messenger subscriber in Marketing Master IO. |
| [Add Subscriber User Data](actions/add-subscriber-user-data.md) | PUT | Adds user data to a Messenger subscriber in Marketing Master IO. |
| [Get Messenger Subscriber](actions/get-messenger-subscriber.md) | GET | Retrieves a Messenger subscriber from Marketing Master IO. |
| [List Messenger Subscribers](actions/list-messenger-subscribers.md) | GET | Retrieves Messenger subscribers from Marketing Master IO. |
| [Remove Subscriber Tag](actions/remove-subscriber-tag.md) | PUT | Removes a tag from a Messenger subscriber in Marketing Master IO. |
| [Remove Subscriber User Data](actions/remove-subscriber-user-data.md) | PUT | Removes user data from a Messenger subscriber in Marketing Master IO. |

