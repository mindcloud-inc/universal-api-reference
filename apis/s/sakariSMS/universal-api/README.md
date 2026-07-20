# <img src="https://images.mindcloud.co/apps/icons/images_1773776373065.jpeg" alt="Sakari SMS logo" width="28" height="28"> Sakari SMS: Universal API

Send SMS campaigns and manage contacts, forms, and webhooks

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sakariSMS/latest
- **Category:** Marketing
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://sakari.io
- **Vendor API docs:** https://developer.sakari.io/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Messages](actions/list-messages.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/list-messages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Create And Execute Campaign](actions/create-and-execute-campaign.md) | POST | Creates and launches a campaign in Sakari SMS. |
| [Create Campaign](actions/create-campaign.md) | POST | Creates a new campaign in Sakari SMS. |
| [Delete Campaign](actions/delete-campaign.md) | DELETE | Deletes an existing campaign from Sakari SMS. |
| [Get Campaign by ID](actions/get-campaign-by-id.md) | GET | Retrieves a campaign from Sakari SMS. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves account campaigns from Sakari SMS. |
| [Update Campaign](actions/update-campaign.md) | PUT | Updates an existing campaign in Sakari SMS. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Sakari SMS. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from Sakari SMS. |
| [Get Contact by ID](actions/get-contact-by-id.md) | GET | Retrieves a contact from Sakari SMS. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves account contacts from Sakari SMS. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Sakari SMS. |

### Conversations

| Action | Method | Description |
| --- | --- | --- |
| [Close Conversation](actions/close-conversation.md) | PUT | Closes a conversation in Sakari SMS. |
| [Get Conversation by ID](actions/get-conversation-by-id.md) | GET | Retrieves a conversation from Sakari SMS. |
| [List Conversations](actions/list-conversations.md) | GET | Retrieves account conversations from Sakari SMS. |

### Form Submissions

| Action | Method | Description |
| --- | --- | --- |
| [Get Lead Form Conversion Data](actions/get-lead-form-conversion-data.md) | GET | Retrieves lead form conversion data from Sakari SMS. |

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [Activate Existing Form](actions/activate-existing-form.md) | PUT | Activates an existing lead form in Sakari SMS. |
| [Create Lead Form](actions/create-lead-form.md) | POST | Creates a new lead form in Sakari SMS. |
| [Deactivate Existing Form](actions/deactivate-existing-form.md) | PUT | Deactivates an existing lead form in Sakari SMS. |
| [Delete Lead Form](actions/delete-lead-form.md) | DELETE | Deletes an existing lead form from Sakari SMS. |
| [Get Lead Form](actions/get-lead-form.md) | GET | Retrieves a lead form from Sakari SMS. |
| [List Lead Forms](actions/list-lead-forms.md) | GET | Retrieves lead forms from Sakari SMS. |
| [Update Lead Form](actions/update-lead-form.md) | PUT | Updates an existing lead form in Sakari SMS. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [List Messages](actions/list-messages.md) | GET | Retrieves account messages from Sakari SMS. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Get Message by ID](actions/get-message-by-id.md) | GET | Retrieves a message from Sakari SMS. |
| [Send Messages](actions/send-messages.md) | POST | Sends text messages through Sakari SMS. |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves an account from Sakari SMS. |
| [Get Account Balance](actions/get-account-balance.md) | GET | Retrieves an account balance from Sakari SMS. |

### Phone Numbers

| Action | Method | Description |
| --- | --- | --- |
| [List Available Phone Numbers](actions/list-available-phone-numbers.md) | GET | Finds available phone numbers in Sakari SMS. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Lead Form Analytic Data](actions/get-lead-form-analytic-data.md) | GET | Retrieves lead form analytics from Sakari SMS. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [Create Template](actions/create-template.md) | POST | Creates a new template in Sakari SMS. |
| [Delete Template](actions/delete-template.md) | DELETE | Deletes an existing template from Sakari SMS. |
| [Get Template by ID](actions/get-template-by-id.md) | GET | Retrieves a template from Sakari SMS. |
| [List Lead Form Templates](actions/list-lead-form-templates.md) | GET | Retrieves lead form templates from Sakari SMS. |
| [List Templates](actions/list-templates.md) | GET | Retrieves account templates from Sakari SMS. |
| [Update Template](actions/update-template.md) | PUT | Updates an existing template in Sakari SMS. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Link by ID](actions/get-link-by-id.md) | GET | Retrieves a link from Sakari SMS. |
| [List Link Sources](actions/list-link-sources.md) | GET | Retrieves link sources from Sakari SMS. |
| [List Links](actions/list-links.md) | GET | Retrieves account links from Sakari SMS. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [List Active Webhooks](actions/list-active-webhooks.md) | GET | Retrieves active webhooks from Sakari SMS. |
| [Subscribe To Message Events](actions/subscribe-to-message-events.md) | POST | Subscribes to message events in Sakari SMS. |

