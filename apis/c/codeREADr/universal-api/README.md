# <img src="https://images.mindcloud.co/apps/icons/code-readr_1774555962515.png" alt="CodeREADr logo" width="28" height="28"> CodeREADr: Universal API

Manage CodeREADr barcode-scanning resources including users, services, databases, questions, and scans through the official Developer API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/codeREADr/latest
- **Category:** Support / Field Service
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.codereadr.com
- **Vendor API docs:** https://secure.codereadr.com/apidocs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Retrieve Limits](actions/retrieve-limits.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codeREADr/latest/actions/retrieve-limits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Database

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Upsert Database Values](actions/bulk-upsert-database-values.md) | PUT | Adds or updates multiple database values in CodeREADr. |

### Databases

| Action | Method | Description |
| --- | --- | --- |
| [Clear Database](actions/clear-database.md) | PUT | Clears all values from a validation database in CodeREADr. |
| [Create Database](actions/create-database.md) | POST | Creates a new validation database in CodeREADr. |
| [Delete Database](actions/delete-database.md) | DELETE | Deletes an existing validation database from CodeREADr. |
| [Delete Database Value](actions/delete-database-value.md) | DELETE | Deletes a database value from CodeREADr. |
| [List Database Values](actions/list-database-values.md) | GET | Retrieves values from a validation database in CodeREADr. |
| [List Databases](actions/list-databases.md) | GET | Retrieves validation databases from your CodeREADr account. |
| [Update Database](actions/update-database.md) | PUT | Updates an existing validation database in CodeREADr. |
| [Upsert Database Value](actions/upsert-database-value.md) | PUT | Adds or updates a database value in CodeREADr. |

### Question

| Action | Method | Description |
| --- | --- | --- |
| [Create Question](actions/create-question.md) | POST | Creates a new data collection question in CodeREADr. |
| [List Questions](actions/list-questions.md) | GET | Retrieves data collection questions from CodeREADr. |

### Scan

| Action | Method | Description |
| --- | --- | --- |
| [List Scans](actions/list-scans.md) | GET | Retrieves barcode scan records from CodeREADr. |

### Services

| Action | Method | Description |
| --- | --- | --- |
| [Add Question to Service](actions/add-question-to-service.md) | PUT | Adds a question to a scanning service in CodeREADr. |
| [Authorize User for Service](actions/authorize-user-for-service.md) | PUT | Authorizes an app user for a scanning service in CodeREADr. |
| [Create Service](actions/create-service.md) | POST | Creates a new scanning service in CodeREADr. |
| [Delete Service](actions/delete-service.md) | DELETE | Deletes an existing scanning service from CodeREADr. |
| [List Services](actions/list-services.md) | GET | Retrieves barcode scanning services from CodeREADr. |
| [Revoke User from Service](actions/revoke-user-from-service.md) | PUT | Revokes an app user's access to a scanning service in CodeREADr. |
| [Update Service](actions/update-service.md) | PUT | Updates an existing scanning service in CodeREADr. |

### Unknown Object

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Limits](actions/retrieve-limits.md) | GET | Retrieves API usage limits from CodeREADr. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a new app user in CodeREADr. |
| [Delete User](actions/delete-user.md) | DELETE | Deletes an existing app user from CodeREADr. |
| [List Users](actions/list-users.md) | GET | Retrieves authorized app users from CodeREADr. |
| [Update User](actions/update-user.md) | PUT | Updates an existing app user in CodeREADr. |

