# <img src="https://images.mindcloud.co/apps/icons/castor_1776717956781.png" alt="Castor EDC logo" width="28" height="28"> Castor EDC: Universal API

Access Castor EDC studies, users, participants, records, forms, and clinical data through the official Castor EDC API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/castorEDC/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 36
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.castoredc.com/
- **Vendor API docs:** https://us.castoredc.com/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/castorEDC/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (36)

### Datasets

| Action | Method | Description |
| --- | --- | --- |
| [Export Study Data](actions/export-study-data.md) | GET | Exports study data from Castor EDC as a dataset. |
| [Export Study Structure](actions/export-study-structure.md) | GET | Exports study structure from Castor EDC as a dataset. |

### Field

| Action | Method | Description |
| --- | --- | --- |
| [Get Field](actions/get-field.md) | GET | Retrieves a field from Castor EDC by ID. |
| [List Fields](actions/list-fields.md) | GET | Retrieves fields from a study in Castor EDC. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Download Export](actions/download-export.md) | GET | Downloads an export file from Castor EDC. |

### Form

| Action | Method | Description |
| --- | --- | --- |
| [Get Form](actions/get-form.md) | GET | Retrieves a form from Castor EDC by ID. |
| [List Forms](actions/list-forms.md) | GET | Retrieves forms from a study in Castor EDC. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Add Study User](actions/add-study-user.md) | POST | Adds a user to a study in Castor EDC. |
| [Create Participant](actions/create-participant.md) | POST | Creates a participant in Castor EDC. |
| [Create Record](actions/create-record.md) | POST | Creates a record in Castor EDC. |
| [Get Participant](actions/get-participant.md) | GET | Retrieves a participant from Castor EDC by ID. |
| [Get Query](actions/get-query.md) | GET | Retrieves a query from Castor EDC by ID. |
| [Get Record](actions/get-record.md) | GET | Retrieves a record from Castor EDC by ID. |
| [Get Study](actions/get-study.md) | GET | Retrieves a study from Castor EDC by ID. |
| [Get Study Statistics](actions/get-study-statistics.md) | GET | Retrieves study statistics from Castor EDC by study ID. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Castor EDC by ID. |
| [List Export Jobs](actions/list-export-jobs.md) | GET | Retrieves export jobs from Castor EDC by study. |
| [List Participants](actions/list-participants.md) | GET | Retrieves study participants from Castor EDC. |
| [List Records](actions/list-records.md) | GET | Retrieves study records from Castor EDC. |
| [List Studies](actions/list-studies.md) | GET | Retrieves studies the current Castor EDC user can access. |
| [List Study Users](actions/list-study-users.md) | GET | Retrieves study users from Castor EDC by study ID. |
| [Request Multi Export](actions/request-multi-export.md) | POST | Requests multiple study exports in Castor EDC. |

### Queries

| Action | Method | Description |
| --- | --- | --- |
| [List Queries](actions/list-queries.md) | GET | Retrieves study queries from Castor EDC. |

### Repeating Data

| Action | Method | Description |
| --- | --- | --- |
| [List Repeating Data Definitions](actions/list-repeating-data-definitions.md) | GET | Retrieves repeating data definitions from Castor EDC. |

### Repeating Data Instance

| Action | Method | Description |
| --- | --- | --- |
| [List Participant Repeating Data Instances](actions/list-participant-repeating-data-instances.md) | GET | Retrieves repeating data instances for a participant in Castor EDC. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [List Reports](actions/list-reports.md) | GET | Retrieves reports from a study in Castor EDC. |

### Study Data Point

| Action | Method | Description |
| --- | --- | --- |
| [Get Participant Study Data Collection](actions/get-participant-study-data-collection.md) | GET | Retrieves study data for a participant in Castor EDC. |
| [Upsert Participant Study Data Collection](actions/upsert-participant-study-data-collection.md) | PUT | Updates participant study data in Castor EDC. |

### Study User

| Action | Method | Description |
| --- | --- | --- |
| [Remove Study User](actions/remove-study-user.md) | DELETE | Deletes a study user from Castor EDC. |
| [Replace Study User Roles](actions/replace-study-user-roles.md) | PUT | Updates study user roles in Castor EDC. |

### Survey

| Action | Method | Description |
| --- | --- | --- |
| [List Surveys](actions/list-surveys.md) | GET | Retrieves surveys from a study in Castor EDC. |

### Survey Package

| Action | Method | Description |
| --- | --- | --- |
| [List Survey Packages](actions/list-survey-packages.md) | GET | Retrieves survey packages from a study in Castor EDC. |

### Survey Package Instance

| Action | Method | Description |
| --- | --- | --- |
| [Create Survey Package Instance](actions/create-survey-package-instance.md) | POST | Creates a survey package instance in Castor EDC. |
| [List Survey Package Instances](actions/list-survey-package-instances.md) | GET | Retrieves survey package instances from Castor EDC. |
| [Update Survey Package Instance](actions/update-survey-package-instance.md) | PUT | Updates a survey package instance in Castor EDC. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves users the current Castor EDC user can access. |

