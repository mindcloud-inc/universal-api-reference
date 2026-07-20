# <img src="https://images.mindcloud.co/apps/icons/microsoft365people_1776176076465.png" alt="Microsoft 365 People logo" width="28" height="28"> Microsoft 365 People: Universal API

Work with Microsoft 365 people and Outlook contacts through Microsoft Graph.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/microsoft365People/latest
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.microsoft365.com
- **Vendor API docs:** https://learn.microsoft.com/en-us/graph/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List People](actions/list-people.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoft365People/latest/actions/list-people?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Microsoft 365 People. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from Microsoft 365 People. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Microsoft 365 People. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Microsoft 365 People. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Microsoft 365 People. |

### People

| Action | Method | Description |
| --- | --- | --- |
| [List People](actions/list-people.md) | GET | Retrieves relevant people from Microsoft 365 People. |

