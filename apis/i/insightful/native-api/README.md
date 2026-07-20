# Insightful: Native API Reference

A consolidated summary of Insightful's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developers.insightful.io/
- **API base URL:** `https://app.insightful.io/api/v1`

## Authentication

### API Key

Use an Insightful API token from Settings -> API Tokens.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.insightful.io/en/articles/4131022-get-api-collections-using-postman)

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | `POST /project` | [docs](https://developers.insightful.io/#4566c05a-bd50-459f-8f0c-e35975c44130) |
| [Create Shared Setting](actions/create-shared-setting.md) | `POST /shared-settings` | [docs](https://developers.insightful.io/#2f30e38e-b5b3-4788-a88d-58ce3d340d41) |
| [Create Task](actions/create-task.md) | `POST /task` | [docs](https://developers.insightful.io/#dd6b68d5-5e70-4404-91bc-ea9898aefb90) |
| [Create Team](actions/create-team.md) | `POST /team` | [docs](https://developers.insightful.io/#6ad29832-4a3f-4af4-8138-c7ede6ab847b) |
| [Create Time Limit](actions/create-time-limit.md) | `POST /time-limit` | [docs](https://developers.insightful.io/#a3fd95eb-18b7-40c2-a611-48d5f07c12cc) |
| [Deactivate Employee](actions/deactivate-employee.md) | `GET /employee/deactivate/:id` | [docs](https://developers.insightful.io/#00bba9e5-2acf-495f-91a2-4e2537fdc088) |
| [Delete Project](actions/delete-project.md) | `DELETE /project/:id` | [docs](https://developers.insightful.io/#79a6fd9e-9bae-4df9-b8af-1c1c09d2b822) |
| [Delete Task](actions/delete-task.md) | `DELETE /task/:id` | [docs](https://developers.insightful.io/#31b7d0ba-a56f-44fd-b152-4aa4f734b8fb) |
| [Delete Team](actions/delete-team.md) | `DELETE /team/:id` | [docs](https://developers.insightful.io/#4fffc1b6-9f90-4558-b214-8118e525cd2d) |
| [Get Employee](actions/get-employee.md) | `GET /employee/:id` | [docs](https://developers.insightful.io/#9658df96-d8e0-49c9-a5dc-685b555e5307) |
| [Get Project](actions/get-project.md) | `GET /project/:id` | [docs](https://developers.insightful.io/#27bce92b-9d4b-41d2-90da-a6fe2574904e) |
| [Get Shared Setting](actions/get-shared-setting.md) | `GET /shared-settings/:id` | [docs](https://developers.insightful.io/#c0c6f6d0-0017-4114-a61a-56d46140a7ec) |
| [Get Task](actions/get-task.md) | `GET /task/:id` | [docs](https://developers.insightful.io/#2b7c9227-7292-4b62-86be-2119de8e811d) |
| [Get Team](actions/get-team.md) | `GET /team/:id` | [docs](https://developers.insightful.io/#1c552e5f-fd75-4160-8262-5622c5f022d7) |
| [Invite Employee](actions/invite-employee.md) | `POST /employee` | [docs](https://developers.insightful.io/#58c5ec14-20c1-4d31-bb79-61420e26ebd9) |
| [List Employees](actions/list-employees.md) | `GET /employee` | [docs](https://developers.insightful.io/#8d5b35bb-b93e-424b-8e65-83e88e671cf0) |
| [List Projects](actions/list-projects.md) | `GET /project` | [docs](https://developers.insightful.io/#8b5efd55-f8ef-4a01-9239-fe2fad79c60c) |
| [List Shared Settings](actions/list-shared-settings.md) | `GET /shared-settings` | [docs](https://developers.insightful.io/#1d9a2170-11e8-49c8-b4a0-2c6c0be88b05) |
| [List Tasks](actions/list-tasks.md) | `GET /task` | [docs](https://developers.insightful.io/#f962fe04-7d38-4c3b-88c0-a22793e2e8f8) |
| [List Teams](actions/list-teams.md) | `GET /team` | [docs](https://developers.insightful.io/#086261a4-ef6a-45b8-8a05-323e4890c46d) |
| [List Time Limits](actions/list-time-limits.md) | `GET /time-limit` | [docs](https://developers.insightful.io/#bdafd15c-8d56-4e87-9ca4-551d2df8b79f) |
| [Update Project](actions/update-project.md) | `PUT /project/:id` | [docs](https://developers.insightful.io/#4a5f4df0-97cb-438e-af9f-9a762235c524) |
| [Update Task](actions/update-task.md) | `PUT /task/:id` | [docs](https://developers.insightful.io/#f0ebc231-a938-4679-a6ce-940cc137cb7a) |
| [Update Team](actions/update-team.md) | `PUT /team/:id` | [docs](https://developers.insightful.io/#dab41be7-d81a-46fc-8903-5120f8d15b42) |
