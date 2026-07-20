# <img src="https://images.mindcloud.co/apps/icons/favicon-www-smapone-com-48x48_1777908861887.png" alt="smapOne logo" width="28" height="28"> smapOne: Universal API

Retrieve smapOne smaps, versions, records, files, tasks, datasources, categories, and SCIM users/groups through the smapOne platform REST APIs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/smapOne/latest
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.smapone.com
- **Vendor API docs:** https://platform.smapone.com/swagger

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List smaps](actions/list-smaps.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/list-smaps?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get account](actions/get-account.md) | GET | Retrieves the current account from smapOne. |

### Account Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get account stats](actions/get-account-stats.md) | GET | Retrieves account statistics from smapOne. |

### Category Smaps

| Action | Method | Description |
| --- | --- | --- |
| [Get category smaps](actions/get-category-smaps.md) | GET | Retrieves smaps in a category from smapOne. |

### Data Record

| Action | Method | Description |
| --- | --- | --- |
| [Delete record](actions/delete-record.md) | DELETE | Deletes an existing data record from smapOne. |
| [Get record](actions/get-record.md) | GET | Retrieves a data record from smapOne. |
| [List records](actions/list-records.md) | GET | Retrieves data records from smapOne. |

### Data Records

| Action | Method | Description |
| --- | --- | --- |
| [Delete records](actions/delete-records.md) | DELETE | Deletes data records from a smapOne version. |

### Datasource

| Action | Method | Description |
| --- | --- | --- |
| [Get datasource](actions/get-datasource.md) | GET | Retrieves a data source from smapOne. |
| [List datasources](actions/list-datasources.md) | GET | Retrieves data sources from smapOne. |

### Datasource Values

| Action | Method | Description |
| --- | --- | --- |
| [Get datasource values](actions/get-datasource-values.md) | GET | Retrieves data source values from smapOne. |

### Datasource Version

| Action | Method | Description |
| --- | --- | --- |
| [List datasource versions](actions/list-datasource-versions.md) | GET | Retrieves data source versions from smapOne. |

### Record File

| Action | Method | Description |
| --- | --- | --- |
| [Get record file](actions/get-record-file.md) | GET | Retrieves a record file from smapOne. |
| [List record files](actions/list-record-files.md) | GET | Retrieves record file metadata from smapOne. |

### Smap

| Action | Method | Description |
| --- | --- | --- |
| [Get smap](actions/get-smap.md) | GET | Retrieves a smap from smapOne. |
| [List smaps](actions/list-smaps.md) | GET | Retrieves smaps from smapOne. |

### Smap Category

| Action | Method | Description |
| --- | --- | --- |
| [List categories](actions/list-categories.md) | GET | Retrieves smap categories from smapOne. |

### Smap Category Assignment

| Action | Method | Description |
| --- | --- | --- |
| [Get smap categories](actions/get-smap-categories.md) | GET | Retrieves categories for a smap from smapOne. |

### Smap Overview

| Action | Method | Description |
| --- | --- | --- |
| [List smap overview](actions/list-smap-overview.md) | GET | Retrieves smap overview metadata from smapOne. |

### Smap Template

| Action | Method | Description |
| --- | --- | --- |
| [List templates](actions/list-templates.md) | GET | Retrieves smap templates from smapOne. |

### Smap Version

| Action | Method | Description |
| --- | --- | --- |
| [List smap versions](actions/list-smap-versions.md) | GET | Retrieves smap versions from smapOne. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create task](actions/create-task.md) | POST | Creates a new task in smapOne. |
| [Update task state](actions/update-task-state.md) | PUT | Updates an existing task state in smapOne. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List users](actions/list-users.md) | GET | Retrieves users from smapOne. |

