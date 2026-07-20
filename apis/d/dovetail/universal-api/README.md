# <img src="https://images.mindcloud.co/apps/icons/dovetail_1773756769774.png" alt="Dovetail logo" width="28" height="28"> Dovetail: Universal API

Manage projects, folders, and research data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dovetail/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://dovetail.com
- **Vendor API docs:** https://developers.dovetail.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dovetail/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in your Dovetail workspace. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from Dovetail. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Dovetail by ID. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from your Dovetail workspace. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Dovetail. |

### Data

| Action | Method | Description |
| --- | --- | --- |
| [Create Data](actions/create-data.md) | POST | Creates a new data entry in Dovetail. |
| [Delete Data](actions/delete-data.md) | DELETE | Deletes an existing data entry from Dovetail. |
| [Get Data](actions/get-data.md) | GET | Retrieves a data entry from Dovetail by ID. |
| [List Data](actions/list-data.md) | GET | Retrieves data entries from your Dovetail workspace. |
| [Update Data](actions/update-data.md) | PUT | Updates an existing data entry in Dovetail. |

### Doc

| Action | Method | Description |
| --- | --- | --- |
| [Create Doc](actions/create-doc.md) | POST | Creates a new doc in your Dovetail workspace. |
| [Delete Doc](actions/delete-doc.md) | DELETE | Deletes an existing doc from Dovetail. |
| [Get Doc](actions/get-doc.md) | GET | Retrieves a doc from Dovetail by ID. |
| [List Docs](actions/list-docs.md) | GET | Retrieves docs from your Dovetail workspace. |
| [Update Doc](actions/update-doc.md) | PUT | Updates an existing doc in Dovetail. |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST | Creates a new folder in your Dovetail workspace. |
| [Delete Folder](actions/delete-folder.md) | DELETE | Deletes an existing folder from Dovetail. |
| [Get Folder](actions/get-folder.md) | GET | Retrieves a folder from Dovetail by ID. |
| [List Folders](actions/list-folders.md) | GET | Retrieves folders from your Dovetail workspace. |
| [Update Folder](actions/update-folder.md) | PUT | Updates an existing folder in Dovetail. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in your Dovetail workspace. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes an existing project from Dovetail. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Dovetail by ID. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from your Dovetail workspace. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Dovetail. |

