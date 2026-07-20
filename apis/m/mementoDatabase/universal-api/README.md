# <img src="https://images.mindcloud.co/apps/icons/memento-database_1774529998734.png" alt="Memento Database logo" width="28" height="28"> Memento Database: Universal API

Manage Memento libraries and records.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mementoDatabase/latest
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://mementodatabase.com
- **Vendor API docs:** https://mementodatabase.docs.apiary.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Libraries](actions/list-libraries.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mementoDatabase/latest/actions/list-libraries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Entry

| Action | Method | Description |
| --- | --- | --- |
| [Create Entry](actions/create-entry.md) | POST | Creates a new entry in a Memento Database library. |
| [Delete Entry](actions/delete-entry.md) | DELETE | Deletes an existing entry from a Memento Database library. |
| [Get Entry](actions/get-entry.md) | GET | Retrieves an entry from a Memento Database library. |
| [List Entries](actions/list-entries.md) | GET | Retrieves entries from a library in Memento Database. |
| [Update Entry](actions/update-entry.md) | PUT | Updates an existing entry in a Memento Database library. |

### Library

| Action | Method | Description |
| --- | --- | --- |
| [Get Library](actions/get-library.md) | GET | Retrieves a library from Memento Database. |
| [List Libraries](actions/list-libraries.md) | GET | Retrieves all libraries from Memento Database. |

