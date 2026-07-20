# Leiga: Native API Reference

A consolidated summary of Leiga's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984
- **API base URL:** `https://app.leiga.com/openapi/api`

## Authentication

### Permanent Access Token

Use a Leiga permanent access token generated from the official Get Permanent Token endpoint.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
accessToken: <apiKey>
```

[Official authentication documentation](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741819.md)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Issue Relation](actions/add-issue-relation.md) | `POST /issue/add-relationship` | [docs](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741849.md) |
| [Add Project Members](actions/add-project-members.md) | `POST /user/add-members` | [docs](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741814.md) |
| [Batch Add Issue](actions/batch-add-issue.md) | `POST /issue/batch-add` | [docs](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-4700177.md) |
| [Batch Add Subtasks](actions/batch-add-subtasks.md) | `POST /issue/batch-add-subtask` | [docs](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741847.md) |
| [Batch Update Issue](actions/batch-update-issue.md) | `PATCH /issue/batch-update` | [docs](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-4700178.md) |
| [Create Comment](actions/create-comment.md) | `POST /comment/add` | [docs](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741893.md) |
| [Create Issue](actions/create-issue.md) | `POST /issue/add` | [docs](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741833.md) |
| [Create Project](actions/create-project.md) | `POST /project/add` | [docs](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741824.md) |
| [Create Sprint](actions/create-sprint.md) | `POST /sprint/add` | [docs](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741855.md) |
| [Get Issue by Issue Number](actions/get-issue-by-issue-number.md) | `GET /issue/get-by-issue-number` | [docs](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741837.md) |
| [Get Issue Detail V2](actions/get-issue-detail-v2.md) | `GET /issue/v2/get` | [docs](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-4820314.md) |
| [Get Issue Field Detail](actions/get-issue-field-detail.md) | `GET /issue/issue-field-info` | [docs](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741836.md) |
| [Get Issue Scheme](actions/get-issue-scheme.md) | `GET /issue/issue-scheme` | [docs](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741834.md) |
| [Get Project](actions/get-project.md) | `GET /project/get` | [docs](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741827.md) |
| [Get Project by Project Key](actions/get-project-by-project-key.md) | `GET /project/get-by-project-key` | [docs](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741828.md) |
| [Get Sprint](actions/get-sprint.md) | `GET /sprint/get` | [docs](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741861.md) |
| [List Comments](actions/list-comments.md) | `POST /comment/page` | [docs](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741900.md) |
| [List Issue Fields](actions/list-issue-fields.md) | `GET /issue/issue-fields` | [docs](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741830.md) |
| [List Issue Relations](actions/list-issue-relations.md) | `GET /issue/relationship-list` | [docs](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741841.md) |
| [List Issue Select Options](actions/list-issue-select-options.md) | `POST /issue/select-options` | [docs](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741842.md) |
| [List Issue Types](actions/list-issue-types.md) | `GET /issue/type-list` | [docs](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741831.md) |
| [List Project Issue Filter Fields](actions/list-project-issue-filter-fields.md) | `POST /issue/filter-condition-field` | [docs](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741840.md) |
| [List Project Members](actions/list-project-members.md) | `GET /user/project-user-page` | [docs](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741826.md) |
| [List Project Sprints](actions/list-project-sprints.md) | `POST /sprint/list-with-count` | [docs](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741860.md) |
| [List Project Workflows](actions/list-project-workflows.md) | `POST /workflow/list` | [docs](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741859.md) |
| [List Projects](actions/list-projects.md) | `GET /project/list` | [docs](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741813.md) |
| [List State Transitions](actions/list-state-transitions.md) | `POST /workflow/list/next-state` | [docs](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741858.md) |
| [List Subtasks](actions/list-subtasks.md) | `POST /issue/list-subtask` | [docs](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741848.md) |
| [Remove Issue](actions/remove-issue.md) | `DELETE /issue/remove` | [docs](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741838.md) |
| [Remove Issue Relation](actions/remove-issue-relation.md) | `POST /issue/remove-relationship` | [docs](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741845.md) |
| [Remove Project Members](actions/remove-project-members.md) | `DELETE /user/remove-members` | [docs](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741815.md) |
| [Remove Subtask](actions/remove-subtask.md) | `DELETE /issue/remove-subtask` | [docs](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741843.md) |
| [Search Issues](actions/search-issues.md) | `POST /issue/page` | [docs](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741839.md) |
| [Search Issues V2](actions/search-issues-v2.md) | `POST /issue/v2/page` | [docs](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-4700180.md) |
| [Update Issue](actions/update-issue.md) | `PATCH /issue/update` | [docs](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741832.md) |
| [Update Project](actions/update-project.md) | `PATCH /project/update` | [docs](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741817.md) |
| [Update Project Member Roles](actions/update-project-member-roles.md) | `POST /project/role-change` | [docs](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741822.md) |
| [Update Sprint](actions/update-sprint.md) | `PATCH /sprint/update` | [docs](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741852.md) |
| [Update Subtask](actions/update-subtask.md) | `PATCH /issue/update-subtask` | [docs](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741844.md) |
| [Update Subtask Status](actions/update-subtask-status.md) | `PATCH /issue/update-subtask-status` | [docs](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741846.md) |
