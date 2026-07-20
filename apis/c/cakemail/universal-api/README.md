# <img src="https://images.mindcloud.co/apps/icons/favicon-cakemail-dev-48x48_1777919255236.png" alt="Cakemail logo" width="28" height="28"> Cakemail: Universal API

Cakemail is an email marketing and transactional email platform for managing audiences, campaigns, senders, forms, templates, reports, and email delivery through its REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cakemail/latest
- **Category:** Marketing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.cakemail.com
- **Vendor API docs:** https://cakemail.dev/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Details](actions/get-account-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cakemail/latest/actions/get-account-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Details](actions/get-account-details.md) | GET | Retrieves the current account details from Cakemail. |

### Account Report

| Action | Method | Description |
| --- | --- | --- |
| [Show My Account Report](actions/show-my-account-report.md) | GET | Retrieves the current account report from Cakemail. |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves all email campaigns from Cakemail. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Add Contact](actions/add-contact.md) | POST | Creates a new contact in a Cakemail list. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes a contact from a Cakemail list. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from a Cakemail list. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from a Cakemail list. |
| [Tag Contact](actions/tag-contact.md) | PUT | Updates tags on a contact in Cakemail. |
| [Unsubscribe Contact](actions/unsubscribe-contact.md) | PUT | Unsubscribes a contact from a Cakemail list. |
| [Untag Contact](actions/untag-contact.md) | PUT | Removes tags from a contact in Cakemail. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in a Cakemail list. |

### Contact Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact Tag](actions/create-contact-tag.md) | POST | Creates a new contact tag in Cakemail. |
| [Delete Contact Tag](actions/delete-contact-tag.md) | DELETE | Deletes a contact tag from Cakemail. |
| [Edit Contact Tag](actions/edit-contact-tag.md) | PUT | Updates an existing contact tag in Cakemail. |
| [List Contact Tags](actions/list-contact-tags.md) | GET | Retrieves all contact tags from Cakemail. |
| [Show Contact Tag](actions/show-contact-tag.md) | GET | Retrieves a contact tag from Cakemail. |

### Domain Validation

| Action | Method | Description |
| --- | --- | --- |
| [Validate Domains](actions/validate-domains.md) | GET | Validates the default sending domains in Cakemail. |

### Email Activity Log

| Action | Method | Description |
| --- | --- | --- |
| [Show Email Activity Logs](actions/show-email-activity-logs.md) | GET | Retrieves email activity logs from Cakemail. |

### List

| Action | Method | Description |
| --- | --- | --- |
| [Archive List](actions/archive-list.md) | DELETE | Archives an existing list in Cakemail. |
| [Create List](actions/create-list.md) | POST | Creates a new list in Cakemail. |
| [Get List](actions/get-list.md) | GET | Retrieves a list from Cakemail by list ID. |
| [List Lists](actions/list-lists.md) | GET | Retrieves all mailing lists from Cakemail. |
| [Update List](actions/update-list.md) | PUT | Updates an existing list in Cakemail. |

### Sender

| Action | Method | Description |
| --- | --- | --- |
| [List Senders](actions/list-senders.md) | GET | Retrieves all sender identities from Cakemail. |

