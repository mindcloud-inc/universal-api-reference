# <img src="https://images.mindcloud.co/apps/icons/samrtcat_1774968716840.png" alt="Smartcat logo" width="28" height="28"> Smartcat: Universal API

Create, manage, and translate multilingual content and localization projects

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/smartcat/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.smartcat.com
- **Vendor API docs:** https://developers.smartcat.com/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartcat/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [List MT Engines](actions/list-mt-engines.md) | GET | Retrieves MT engines available for the Smartcat account. |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves account details from the current Smartcat account. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Smartcat. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes an existing project from Smartcat. |
| [Get Project](actions/get-project.md) | GET | Retrieves project details from the Smartcat account. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from the current Smartcat account. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Smartcat. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [List Templates](actions/list-templates.md) | GET | Retrieves templates available in the Smartcat workspace. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Add Project Document](actions/add-project-document.md) | POST | Adds a document to a Smartcat project. |
| [Create Translation Memory](actions/create-translation-memory.md) | POST | Creates a new translation memory in Smartcat. |
| [Delete Documents](actions/delete-documents.md) | DELETE | Deletes documents from the current Smartcat account. |
| [Delete Translation Memory](actions/delete-translation-memory.md) | DELETE | Deletes a translation memory from Smartcat. |
| [Download Document Export](actions/download-document-export.md) | GET | Retrieves document export results from Smartcat. |
| [Get Default Glossary](actions/get-default-glossary.md) | GET | Retrieves the default glossary from the Smartcat account. |
| [Get Document](actions/get-document.md) | GET | Retrieves document details from the Smartcat account. |
| [Get Document Statistics](actions/get-document-statistics.md) | GET | Retrieves document statistics from the Smartcat account. |
| [Get Glossary Import Task Status](actions/get-glossary-import-task-status.md) | GET | Retrieves glossary import task status from Smartcat. |
| [Get Translation Memory](actions/get-translation-memory.md) | GET | Retrieves translation memory details from Smartcat. |
| [Import Glossary](actions/import-glossary.md) | POST | Creates a glossary import task in Smartcat. |
| [List Glossaries](actions/list-glossaries.md) | GET | Retrieves glossaries from the current Smartcat account. |
| [List Translation Memories](actions/list-translation-memories.md) | GET | Retrieves translation memories from the current Smartcat account. |
| [Request Document Export](actions/request-document-export.md) | POST | Creates a document export task in Smartcat. |
| [Request Glossary Export](actions/request-glossary-export.md) | POST | Creates a glossary export task in Smartcat. |
| [Update Document](actions/update-document.md) | PUT | Updates an existing document in Smartcat. |

