# Checkmk: Native API Reference

A consolidated summary of Checkmk's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.checkmk.com/latest/en/rest_api.html
- **OpenAPI specification:** https://docs.checkmk.com/latest/en/rest_api.html
- **API base URL:** `{apiUrl}`

## Authentication

### Checkmk automation secret

Authenticate to the Checkmk REST API with an automation username and automation secret. The runtime sends Authorization: Bearer <username> <automation secret>.

### Credentials

- **API Key:** `apiKey` · required
- **API URL:** `apiUrl` · required · Full Checkmk REST API base URL, ending with /check_mk/api/1.0.
- **Username:** `username` · required · Checkmk automation username.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.checkmk.com/latest/en/rest_api.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `value`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Acknowledge Host Problems](actions/acknowledge-host-problems.md) | `POST /domain-types/acknowledge/collections/host` | [docs](https://github.com/Checkmk/checkmk/tree/master/cmk/gui/openapi/endpoints/acknowledgement) |
| [Activate Changes](actions/activate-changes.md) | `POST /domain-types/activation_run/actions/activate-changes/invoke` | [docs](https://docs.checkmk.com/latest/en/rest_api.html) |
| [Create Folder](actions/create-folder.md) | `POST /domain-types/folder_config/collections/all` | [docs](https://docs.checkmk.com/latest/en/rest_api.html) |
| [Create Host](actions/create-host.md) | `POST /domain-types/host_config/collections/all` | [docs](https://docs.checkmk.com/latest/en/rest_api.html) |
| [Create Host Downtime](actions/create-host-downtime.md) | `POST /domain-types/downtime/collections/host` | [docs](https://github.com/Checkmk/checkmk/tree/master/cmk/gui/openapi/endpoints/downtime) |
| [Create Host Group](actions/create-host-group.md) | `POST /domain-types/host_group_config/collections/all` | [docs](https://github.com/Checkmk/checkmk/tree/master/cmk/gui/openapi/endpoints/host_group_config) |
| [Create Service Group](actions/create-service-group.md) | `POST /domain-types/service_group_config/collections/all` | [docs](https://github.com/Checkmk/checkmk/tree/master/cmk/gui/openapi/endpoints/service_group_config) |
| [Delete Folder](actions/delete-folder.md) | `DELETE /objects/folder_config/{folder}` | [docs](https://docs.checkmk.com/latest/en/rest_api.html) |
| [Delete Host](actions/delete-host.md) | `DELETE /objects/host_config/{host_name}` | [docs](https://docs.checkmk.com/latest/en/rest_api.html) |
| [Delete Host Group](actions/delete-host-group.md) | `DELETE /objects/host_group_config/{name}` | [docs](https://github.com/Checkmk/checkmk/tree/master/cmk/gui/openapi/endpoints/host_group_config) |
| [Get Activation Run](actions/get-activation-run.md) | `GET /objects/activation_run/{activation_id}` | [docs](https://docs.checkmk.com/latest/en/rest_api.html) |
| [Get API Version](actions/get-api-version.md) | `GET /version` | [docs](https://docs.checkmk.com/latest/en/rest_api.html) |
| [Get Folder](actions/get-folder.md) | `GET /objects/folder_config/{folder}` | [docs](https://docs.checkmk.com/latest/en/rest_api.html) |
| [Get Host Config](actions/get-host-config.md) | `GET /objects/host_config/{host_name}` | [docs](https://docs.checkmk.com/latest/en/rest_api.html) |
| [Get Host Group](actions/get-host-group.md) | `GET /objects/host_group_config/{name}` | [docs](https://github.com/Checkmk/checkmk/tree/master/cmk/gui/openapi/endpoints/host_group_config) |
| [List Audit Log](actions/list-audit-log.md) | `GET /domain-types/audit_log/collections/all` | [docs](https://github.com/Checkmk/checkmk/tree/master/cmk/gui/openapi/endpoints/audit_log) |
| [List Downtimes](actions/list-downtimes.md) | `GET /domain-types/downtime/collections/all` | [docs](https://github.com/Checkmk/checkmk/tree/master/cmk/gui/openapi/endpoints/downtime) |
| [List Folder Hosts](actions/list-folder-hosts.md) | `GET /objects/folder_config/{folder}/collections/hosts` | [docs](https://docs.checkmk.com/latest/en/rest_api.html) |
| [List Folders](actions/list-folders.md) | `GET /domain-types/folder_config/collections/all` | [docs](https://docs.checkmk.com/latest/en/rest_api.html) |
| [List Host Configs](actions/list-host-configs.md) | `GET /domain-types/host_config/collections/all` | [docs](https://docs.checkmk.com/latest/en/rest_api.html) |
| [List Host Groups](actions/list-host-groups.md) | `GET /domain-types/host_group_config/collections/all` | [docs](https://github.com/Checkmk/checkmk/tree/master/cmk/gui/openapi/endpoints/host_group_config) |
| [List Host Services](actions/list-host-services.md) | `GET /objects/host/{host_name}/collections/services` | [docs](https://docs.checkmk.com/latest/en/rest_api.html) |
| [List Pending Changes](actions/list-pending-changes.md) | `GET /domain-types/activation_run/collections/pending_changes` | [docs](https://docs.checkmk.com/latest/en/rest_api.html) |
| [List Service Groups](actions/list-service-groups.md) | `GET /domain-types/service_group_config/collections/all` | [docs](https://github.com/Checkmk/checkmk/tree/master/cmk/gui/openapi/endpoints/service_group_config) |
| [List Services](actions/list-services.md) | `GET /domain-types/service/collections/all` | [docs](https://docs.checkmk.com/latest/en/rest_api.html) |
| [Move Host](actions/move-host.md) | `POST /objects/host_config/{host_name}/actions/move/invoke` | [docs](https://docs.checkmk.com/latest/en/rest_api.html) |
| [Rename Host](actions/rename-host.md) | `PUT /objects/host_config/{host_name}/actions/rename/invoke` | [docs](https://docs.checkmk.com/latest/en/rest_api.html) |
| [Show Host Service](actions/show-host-service.md) | `GET /objects/host/{host_name}/actions/show_service/invoke` | [docs](https://docs.checkmk.com/latest/en/rest_api.html) |
| [Update Host](actions/update-host.md) | `PUT /objects/host_config/{host_name}` | [docs](https://docs.checkmk.com/latest/en/rest_api.html) |
| [Update Host Group](actions/update-host-group.md) | `PUT /objects/host_group_config/{name}` | [docs](https://github.com/Checkmk/checkmk/tree/master/cmk/gui/openapi/endpoints/host_group_config) |
