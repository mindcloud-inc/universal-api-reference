# Castor EDC: Native API Reference

A consolidated summary of Castor EDC's API configuration and 36 documented operations, with links to official documentation.

- **Official docs:** https://us.castoredc.com/api
- **OpenAPI specification:** https://us.castoredc.com/api/swagger?format=json
- **API base URL:** `https://us.castoredc.com/api`

## Authentication

### OAuth2 client credentials

OAuth2 client-credentials authentication for the Castor EDC API.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://us.castoredc.com/oauth/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `default`.

A machine-to-machine flow is configured.

[Official authentication documentation](https://helpdesk.castoredc.com/hc/en-us/articles/27149233860509-Castor-EDC-CDMS-Application-Programming-Interface-API)

## API conventions

Responses from this API use JSON. Response data is read from `Embedded.user`.

## Endpoints (36 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Study User](actions/add-study-user.md) | `POST /study/:study_id/user` | [docs](https://us.castoredc.com/api) |
| [Create Participant](actions/create-participant.md) | `POST /study/:study_id/participant` | [docs](https://us.castoredc.com/api) |
| [Create Record](actions/create-record.md) | `POST /study/:study_id/record` | [docs](https://us.castoredc.com/api) |
| [Create Survey Package Instance](actions/create-survey-package-instance.md) | `POST /study/:study_id/survey-package-instance` | [docs](https://us.castoredc.com/api) |
| [Download Export](actions/download-export.md) | `GET /study/:study_id/export/:id/download` | [docs](https://us.castoredc.com/api) |
| [Export Study Data](actions/export-study-data.md) | `GET /study/:study_id/export/data` | [docs](https://us.castoredc.com/api) |
| [Export Study Structure](actions/export-study-structure.md) | `GET /study/:study_id/export/structure` | [docs](https://us.castoredc.com/api) |
| [Get Field](actions/get-field.md) | `GET /study/:study_id/field/:field_id` | [docs](https://us.castoredc.com/api) |
| [Get Form](actions/get-form.md) | `GET /study/:study_id/form/:form_id` | [docs](https://us.castoredc.com/api) |
| [Get Participant](actions/get-participant.md) | `GET /study/:study_id/participant/:participant_id` | [docs](https://us.castoredc.com/api) |
| [Get Participant Study Data Collection](actions/get-participant-study-data-collection.md) | `GET /study/:study_id/participant/:participant_id/data-points/study` | [docs](https://us.castoredc.com/api) |
| [Get Query](actions/get-query.md) | `GET /study/:study_id/query/:query_id` | [docs](https://us.castoredc.com/api) |
| [Get Record](actions/get-record.md) | `GET /study/:study_id/record/:record_id` | [docs](https://us.castoredc.com/api) |
| [Get Study](actions/get-study.md) | `GET /study/:study_id` | [docs](https://us.castoredc.com/api) |
| [Get Study Statistics](actions/get-study-statistics.md) | `GET /study/:study_id/statistics` | [docs](https://us.castoredc.com/api) |
| [Get User](actions/get-user.md) | `GET /user/:user_id` | [docs](https://us.castoredc.com/api) |
| [List Export Jobs](actions/list-export-jobs.md) | `GET /study/:study_id/export` | [docs](https://us.castoredc.com/api) |
| [List Fields](actions/list-fields.md) | `GET /study/:study_id/field` | [docs](https://us.castoredc.com/api) |
| [List Forms](actions/list-forms.md) | `GET /study/:study_id/form` | [docs](https://us.castoredc.com/api) |
| [List Participant Repeating Data Instances](actions/list-participant-repeating-data-instances.md) | `GET /study/:study_id/participant/:participant_id/repeating-data-instance` | [docs](https://us.castoredc.com/api) |
| [List Participants](actions/list-participants.md) | `GET /study/:study_id/participant` | [docs](https://us.castoredc.com/api) |
| [List Queries](actions/list-queries.md) | `GET /study/:study_id/query` | [docs](https://us.castoredc.com/api) |
| [List Records](actions/list-records.md) | `GET /study/:study_id/record` | [docs](https://us.castoredc.com/api) |
| [List Repeating Data Definitions](actions/list-repeating-data-definitions.md) | `GET /study/:study_id/repeating-data` | [docs](https://us.castoredc.com/api) |
| [List Reports](actions/list-reports.md) | `GET /study/:study_id/report` | [docs](https://us.castoredc.com/api) |
| [List Studies](actions/list-studies.md) | `GET /study` | [docs](https://us.castoredc.com/api) |
| [List Study Users](actions/list-study-users.md) | `GET /study/:study_id/user` | [docs](https://us.castoredc.com/api) |
| [List Survey Package Instances](actions/list-survey-package-instances.md) | `GET /study/:study_id/survey-package-instance` | [docs](https://us.castoredc.com/api) |
| [List Survey Packages](actions/list-survey-packages.md) | `GET /study/:study_id/survey-package` | [docs](https://us.castoredc.com/api) |
| [List Surveys](actions/list-surveys.md) | `GET /study/:study_id/survey` | [docs](https://us.castoredc.com/api) |
| [List Users](actions/list-users.md) | `GET /user` | [docs](https://data.castoredc.com/api) |
| [Remove Study User](actions/remove-study-user.md) | `DELETE /study/:study_id/user/:user_id` | [docs](https://us.castoredc.com/api) |
| [Replace Study User Roles](actions/replace-study-user-roles.md) | `PUT /study/:study_id/user/:user_id` | [docs](https://us.castoredc.com/api) |
| [Request Multi Export](actions/request-multi-export.md) | `POST /study/:study_id/export` | [docs](https://us.castoredc.com/api) |
| [Update Survey Package Instance](actions/update-survey-package-instance.md) | `PATCH /study/:study_id/survey-package-instance/:survey_package_instance_id` | [docs](https://us.castoredc.com/api) |
| [Upsert Participant Study Data Collection](actions/upsert-participant-study-data-collection.md) | `POST /study/:study_id/participant/:participant_id/data-points/study` | [docs](https://us.castoredc.com/api) |
