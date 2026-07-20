# <img src="https://images.mindcloud.co/apps/icons/coda_1773239429810.png" alt="Coda logo" width="28" height="28"> Coda: Universal API

Coda: Manage docs, tables, rows, pages, and buttons

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/coda/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://coda.io
- **Vendor API docs:** https://coda.io/developers/apis/v1

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Docs](actions/list-docs.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coda/latest/actions/list-docs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Button

| Action | Method | Description |
| --- | --- | --- |
| [Push Button](actions/push-button.md) | PUT | Pushes a button in a Coda table row. |

### Column

| Action | Method | Description |
| --- | --- | --- |
| [Get Column](actions/get-column.md) | GET | Retrieves column details from a Coda table. |
| [List Columns](actions/list-columns.md) | GET | Retrieves columns from a Coda table. |

### Control

| Action | Method | Description |
| --- | --- | --- |
| [Get Control](actions/get-control.md) | GET | Retrieves control details from a Coda doc. |
| [List Controls](actions/list-controls.md) | GET | Retrieves controls from a Coda doc. |

### Doc

| Action | Method | Description |
| --- | --- | --- |
| [Create Doc](actions/create-doc.md) | POST | Creates a new doc in Coda. |
| [Delete Doc](actions/delete-doc.md) | DELETE | Deletes a doc from a Coda workspace. |
| [Get Doc](actions/get-doc.md) | GET | Retrieves details for a Coda doc. |
| [List Docs](actions/list-docs.md) | GET | Retrieves accessible docs from Coda workspaces. |
| [Update Doc](actions/update-doc.md) | PUT | Updates metadata for a Coda doc. |

### Formula

| Action | Method | Description |
| --- | --- | --- |
| [Get Formula](actions/get-formula.md) | GET | Retrieves formula details from a Coda doc. |
| [List Formulas](actions/list-formulas.md) | GET | Retrieves formulas from a Coda doc. |

### Page

| Action | Method | Description |
| --- | --- | --- |
| [Create Page](actions/create-page.md) | POST | Creates a new page in a Coda doc. |
| [Delete Page](actions/delete-page.md) | DELETE | Deletes a page from a Coda doc. |
| [Get Page](actions/get-page.md) | GET | Retrieves page details from a Coda doc. |
| [List Pages](actions/list-pages.md) | GET | Retrieves pages from a Coda doc. |
| [Update Page](actions/update-page.md) | PUT | Updates a page in a Coda doc. |

### Row

| Action | Method | Description |
| --- | --- | --- |
| [Delete Row](actions/delete-row.md) | DELETE | Deletes a row from a Coda table. |
| [Get Row](actions/get-row.md) | GET | Retrieves row details from a Coda table. |
| [List Rows](actions/list-rows.md) | GET | Retrieves rows from a Coda table. |
| [Update Row](actions/update-row.md) | PUT | Updates a row in a Coda table. |
| [Upsert Rows](actions/upsert-rows.md) | POST | Inserts or updates rows in a Coda table. |

### Table

| Action | Method | Description |
| --- | --- | --- |
| [Get Table](actions/get-table.md) | GET | Retrieves table details from a Coda doc. |
| [List Tables](actions/list-tables.md) | GET | Retrieves tables from a Coda doc. |

