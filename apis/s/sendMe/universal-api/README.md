# <img src="https://images.mindcloud.co/apps/icons/endme_1775142448428.png" alt="SendMe logo" width="28" height="28"> SendMe: Universal API

SendMe API wrapper for managing contacts and sending SMS or email campaigns.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sendMe/latest
- **Category:** Marketing
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://sendme123.com
- **Vendor API docs:** https://docs.sendme123.com/en/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Contacts](actions/list-contacts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendMe/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST |  |
| [Delete Contact](actions/delete-contact.md) | DELETE |  |
| [Get Contact](actions/get-contact.md) | GET |  |
| [List Contacts](actions/list-contacts.md) | GET |  |
| [Update Contact](actions/update-contact.md) | PUT |  |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [List Messages](actions/list-messages.md) | GET |  |
| [Send Email by Tags](actions/send-email-by-tags.md) | POST |  |
| [Send Email to All](actions/send-email-to-all.md) | POST |  |
| [Send Email to Contacts](actions/send-email-to-contacts.md) | POST |  |
| [Send SMS by Tags](actions/send-sms-by-tags.md) | POST |  |
| [Send SMS to All](actions/send-sms-to-all.md) | POST |  |
| [Send SMS to Contacts](actions/send-sms-to-contacts.md) | POST |  |

