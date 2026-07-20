# DataScope Forms: Native API Reference

A consolidated summary of DataScope Forms's API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://dscope.github.io/docs/
- **API base URL:** `https://www.mydatascope.com/api`

## Authentication

### API Key

Authenticate with a DataScope API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://help.mydatascope.com/en/articles/9628405-datascope-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Bulk Update List Elements](actions/bulk-update-list-elements.md) | `POST /external/metadata_objects/bulk_update` | [docs](https://dscope.github.io/docs/#bulk-update-list-elements) |
| [Create List](actions/create-list.md) | `POST /external/metadata_types` | [docs](https://dscope.github.io/docs/#create-a-empty-list) |
| [Create List Element](actions/create-list-element.md) | `POST /external/metadata_object` | [docs](https://dscope.github.io/docs/#create-a-list-element) |
| [Create Location](actions/create-location.md) | `POST /external/locations` | [docs](https://dscope.github.io/docs/#create-a-location) |
| [Create Task Assignment](actions/create-task-assignment.md) | `POST /external/assign_task` | [docs](https://dscope.github.io/docs/#create-task-assign) |
| [Get List Element](actions/get-list-element.md) | `GET /external/metadata_object` | [docs](https://dscope.github.io/docs/#get-an-element-of-the-list) |
| [List Answers](actions/list-answers.md) | `GET /external/v2/answers` | [docs](https://dscope.github.io/docs/#get-all-answers) |
| [List Answers with Metadata](actions/list-answers-with-metadata.md) | `GET /external/answers` | [docs](https://dscope.github.io/docs/#get-all-answers-with-metadata) |
| [List Generated Files](actions/list-generated-files.md) | `GET /external/files` | [docs](https://dscope.github.io/docs/#list-last-generated-files) |
| [List List Elements](actions/list-list-elements.md) | `GET /external/metadata_objects` | [docs](https://dscope.github.io/docs/#get-all-list-elements) |
| [List Locations](actions/list-locations.md) | `GET /external/locations` | [docs](https://dscope.github.io/docs/#get-all-locations) |
| [List Notifications](actions/list-notifications.md) | `GET /external/notifications` | [docs](https://dscope.github.io/docs/#list-last-notifications) |
| [Update List Element](actions/update-list-element.md) | `POST /external/metadata_object/[:id]` | [docs](https://dscope.github.io/docs/#update-a-list-element) |
| [Update Location](actions/update-location.md) | `POST /external/locations/[:id]` | [docs](https://dscope.github.io/docs/#update-a-location) |
