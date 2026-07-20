# <img src="https://images.mindcloud.co/apps/icons/charla_1774898304449.png" alt="Charla logo" width="28" height="28"> Charla: Universal API

Manage contacts, conversations, knowledge base articles, and categories through the Charla Public API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/charla/latest
- **Category:** Support / Ticketing
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://charla.com
- **Vendor API docs:** https://charla.com/public-api.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Contacts](actions/list-contacts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/charla/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Collections

| Action | Method | Description |
| --- | --- | --- |
| [Delete Article](actions/delete-article.md) | DELETE | Deletes an existing article from Charla. |
| [Get Article](actions/get-article.md) | GET | Retrieves an article from Charla. |
| [List Articles](actions/list-articles.md) | GET | Retrieves articles from Charla. |
| [List Categories](actions/list-categories.md) | GET | Retrieves categories from Charla. |
| [Save Article](actions/save-article.md) | POST | Saves an article record in Charla. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Charla. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Charla. |
| [Save Contact](actions/save-contact.md) | POST | Saves a contact record in Charla. |

### Tickets

| Action | Method | Description |
| --- | --- | --- |
| [List Conversations](actions/list-conversations.md) | GET | Retrieves conversations from Charla. |

