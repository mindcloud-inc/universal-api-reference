# <img src="https://images.mindcloud.co/apps/icons/keap-fav_1772814343772.png" alt="Keap logo" width="28" height="28"> Keap: Universal API

Manage contacts, automate follow-ups, send campaigns, and close sales.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/keap/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://keap.com
- **Vendor API docs:** https://developer.keap.com/docs/restv2/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Company](actions/get-company.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/keap/latest/actions/get-company?connectionId=$CONNECTION_ID&company_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | POST |  |
| [Get Company](actions/get-company.md) | GET |  |
| [List Companies](actions/list-companies.md) | GET |  |
| [Update Company](actions/update-company.md) | PUT |  |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [List Contacts](actions/list-contacts.md) | GET |  |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST |  |
| [Delete Contact](actions/delete-contact.md) | DELETE |  |
| [Get Contact](actions/get-contact.md) | GET |  |
| [Update Contact](actions/update-contact.md) | PUT |  |

### Emails

| Action | Method | Description |
| --- | --- | --- |
| [List Emails](actions/list-emails.md) | GET |  |
| [Send Email](actions/send-email.md) | POST |  |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Get File](actions/get-file.md) | GET |  |
| [List Files](actions/list-files.md) | GET |  |

### Notes

| Action | Method | Description |
| --- | --- | --- |
| [Create Note](actions/create-note.md) | POST |  |
| [Get Note](actions/get-note.md) | GET |  |
| [List Notes](actions/list-notes.md) | GET |  |
| [Update Note](actions/update-note.md) | PUT |  |

### Opportunities

| Action | Method | Description |
| --- | --- | --- |
| [Create Opportunity](actions/create-opportunity.md) | POST |  |
| [Get Opportunity](actions/get-opportunity.md) | GET |  |
| [List Opportunities](actions/list-opportunities.md) | GET |  |
| [Update Opportunity](actions/update-opportunity.md) | PUT |  |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Apply Tag To Contacts](actions/apply-tag-to-contacts.md) | PUT |  |
| [Create Tag](actions/create-tag.md) | POST |  |
| [Get Tag](actions/get-tag.md) | GET |  |
| [List Tags](actions/list-tags.md) | GET |  |
| [Remove Tags From Contacts](actions/remove-tags-from-contacts.md) | PUT |  |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST |  |
| [Get Task](actions/get-task.md) | GET |  |
| [List Tasks](actions/list-tasks.md) | GET |  |
| [Update Task](actions/update-task.md) | PUT |  |

