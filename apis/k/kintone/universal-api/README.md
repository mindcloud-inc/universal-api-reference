# <img src="https://images.mindcloud.co/apps/icons/kintone_1773411250782.png" alt="Kintone logo" width="28" height="28"> Kintone: Universal API

Kintone: Build, manage, and automate custom business apps

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/kintone/latest
- **Category:** IT Operations / Database
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.kintone.com/
- **Vendor API docs:** https://kintone.dev/en/docs/kintone/rest-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Apps](actions/list-apps.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kintone/latest/actions/list-apps?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Applications

| Action | Method | Description |
| --- | --- | --- |
| [Add Record](actions/add-record.md) | POST | Creates a record in Kintone. |
| [Add Records](actions/add-records.md) | POST | Creates records in Kintone. |
| [Delete Records](actions/delete-records.md) | DELETE | Deletes existing records from Kintone. |
| [Get Action Settings](actions/get-action-settings.md) | GET | Retrieves action settings from Kintone. |
| [Get App](actions/get-app.md) | GET | Retrieves an app from Kintone. |
| [Get App Permissions](actions/get-app-permissions.md) | GET | Retrieves app permissions from Kintone. |
| [Get Form](actions/get-form.md) | GET | Retrieves an app form from Kintone. |
| [Get Form Fields](actions/get-form-fields.md) | GET | Retrieves app form fields from Kintone. |
| [Get Form Layout](actions/get-form-layout.md) | GET | Retrieves an app form layout from Kintone. |
| [Get General Settings](actions/get-general-settings.md) | GET | Retrieves general app settings from Kintone. |
| [Get Process Management Settings](actions/get-process-management-settings.md) | GET | Retrieves process management settings from Kintone. |
| [Get Record](actions/get-record.md) | GET | Retrieves a record from Kintone. |
| [Get Views](actions/get-views.md) | GET | Retrieves app views from Kintone. |
| [List Apps](actions/list-apps.md) | GET | Retrieves apps from Kintone. |
| [List Records](actions/list-records.md) | GET | Retrieves records from Kintone. |
| [Update Assignees](actions/update-assignees.md) | PUT | Updates record assignees in Kintone. |
| [Update Record](actions/update-record.md) | PUT | Updates an existing record in Kintone. |
| [Update Records](actions/update-records.md) | PUT | Updates existing records in Kintone. |
| [Update Status](actions/update-status.md) | PUT | Updates a record status in Kintone. |
| [Update Statuses](actions/update-statuses.md) | PUT | Updates record statuses in Kintone. |

### Comments

| Action | Method | Description |
| --- | --- | --- |
| [Add Comment](actions/add-comment.md) | POST | Creates a comment on a Kintone record. |
| [List Comments](actions/list-comments.md) | GET | Retrieves comments from a Kintone record. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Download File](actions/download-file.md) | GET | Downloads a file from Kintone. |
| [Upload File](actions/upload-file.md) | POST | Uploads a file to Kintone. |

