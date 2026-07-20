# <img src="https://images.mindcloud.co/apps/icons/icon-2_1776821171461.png" alt="Mailcoach logo" width="28" height="28"> Mailcoach: Universal API

Manage email lists, subscribers, campaigns, and templates

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mailcoach/latest
- **Category:** Communication / Email Communications
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.mailcoach.app
- **Vendor API docs:** https://www.mailcoach.app/api-documentation/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailcoach/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Email List

| Action | Method | Description |
| --- | --- | --- |
| [Create Email List](actions/create-email-list.md) | POST | Creates a new email list in Mailcoach. |
| [Delete Email List](actions/delete-email-list.md) | DELETE | Deletes an email list from Mailcoach. |
| [Get Email List](actions/get-email-list.md) | GET | Retrieves an email list from Mailcoach. |
| [List Email Lists](actions/list-email-lists.md) | GET | Retrieves all email lists from Mailcoach. |
| [Update Email List](actions/update-email-list.md) | PUT | Updates an existing email list in Mailcoach. |

### Subscriber

| Action | Method | Description |
| --- | --- | --- |
| [Add Tags To Subscriber](actions/add-tags-to-subscriber.md) | PUT | Adds tags to a subscriber in Mailcoach. |
| [Confirm Subscriber](actions/confirm-subscriber.md) | PUT | Confirms an existing subscriber in Mailcoach. |
| [Create Subscriber](actions/create-subscriber.md) | POST | Creates a new subscriber in a Mailcoach email list. |
| [Delete Subscriber](actions/delete-subscriber.md) | DELETE | Deletes a subscriber from Mailcoach. |
| [Get Subscriber](actions/get-subscriber.md) | GET | Retrieves a subscriber from Mailcoach. |
| [List Subscribers](actions/list-subscribers.md) | GET | Retrieves subscribers from a Mailcoach email list. |
| [Remove Tags From Subscriber](actions/remove-tags-from-subscriber.md) | PUT | Removes tags from a subscriber in Mailcoach. |
| [Unsubscribe Subscriber](actions/unsubscribe-subscriber.md) | PUT | Unsubscribes an existing subscriber in Mailcoach. |
| [Update Subscriber](actions/update-subscriber.md) | PUT | Updates an existing subscriber in Mailcoach. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Create Template](actions/create-template.md) | POST | Creates a new template in Mailcoach. |
| [Delete Template](actions/delete-template.md) | DELETE | Deletes a template from Mailcoach. |
| [Get Template](actions/get-template.md) | GET | Retrieves a template from Mailcoach. |
| [List Templates](actions/list-templates.md) | GET | Retrieves all templates from Mailcoach. |
| [Update Template](actions/update-template.md) | PUT | Updates an existing template in Mailcoach. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current authenticated user from Mailcoach. |

