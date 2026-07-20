# <img src="https://images.mindcloud.co/apps/icons/webling_1775502618507.png" alt="Webling logo" width="28" height="28"> Webling: Universal API

Manage club members, finances, events, and communication

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/webling/latest
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.webling.ch
- **Vendor API docs:** https://demo.webling.ch/api/1

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webling/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Article

| Action | Method | Description |
| --- | --- | --- |
| [List Articles](actions/list-articles.md) | GET |  |

### Changes

| Action | Method | Description |
| --- | --- | --- |
| [Get Changes After Revision](actions/get-changes-after-revision.md) | GET |  |
| [Get Changes Since Timestamp](actions/get-changes-since-timestamp.md) | GET |  |

### Current User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET |  |

### Debitor

| Action | Method | Description |
| --- | --- | --- |
| [List Debitors](actions/list-debitors.md) | GET |  |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Create Document](actions/create-document.md) | POST |  |
| [Delete Document](actions/delete-document.md) | DELETE |  |
| [Get Document](actions/get-document.md) | GET |  |
| [Get Document Content](actions/get-document-content.md) | GET |  |
| [List Documents](actions/list-documents.md) | GET |  |
| [Update Document](actions/update-document.md) | PUT |  |

### Document Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Documentgroup](actions/create-documentgroup.md) | POST |  |
| [Get Documentgroup](actions/get-documentgroup.md) | GET |  |
| [List Documentgroups](actions/list-documentgroups.md) | GET |  |

### Entry

| Action | Method | Description |
| --- | --- | --- |
| [List Entries](actions/list-entries.md) | GET |  |

### Entry Group

| Action | Method | Description |
| --- | --- | --- |
| [List Entrygroups](actions/list-entrygroups.md) | GET |  |

### Member

| Action | Method | Description |
| --- | --- | --- |
| [List Members](actions/list-members.md) | GET |  |

### Member Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Membergroup](actions/create-membergroup.md) | POST |  |
| [List Membergroups](actions/list-membergroups.md) | GET |  |

### Revision

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Revision](actions/get-current-revision.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET |  |

