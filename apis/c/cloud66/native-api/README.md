# Cloud 66: Native API Reference

A consolidated summary of Cloud 66's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://developers.cloud66.com/v3/
- **API base URL:** `https://app.cloud66.com/api/3`

## Authentication

### API Key

Use a Cloud 66 OAuth access token as a bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.cloud66.com/v3/getting-started/authentication/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `response`.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Environment Variable](actions/add-environment-variable.md) | `POST /stacks/:stack_id/environments` | [docs](https://developers.cloud66.com/v3/endpoints/environment-variables/#add-environment-variable) |
| [Cancel Deployment](actions/cancel-deployment.md) | `DELETE /stacks/:stack_id/deployments/:deployment_id` | [docs](https://developers.cloud66.com/v3/endpoints/deployments/#cancel-deployment) |
| [Create Backup](actions/create-backup.md) | `POST /stacks/:stack_id/backups` | [docs](https://developers.cloud66.com/v3/endpoints/backups/#create-backup) |
| [Create Database](actions/create-database.md) | `POST /stacks/:stack_id/server_groups/:server_group_id/databases` | [docs](https://developers.cloud66.com/v3/endpoints/databases/#create-database) |
| [Create Database User](actions/create-database-user.md) | `POST /stacks/:stack_id/server_groups/:server_group_id/database_users` | [docs](https://developers.cloud66.com/v3/endpoints/database-users/#create-database-user) |
| [Create SSL Certificate](actions/create-ssl-certificate.md) | `POST /stacks/:stack_id/ssl_certificates` | [docs](https://developers.cloud66.com/v3/endpoints/stacks/#ssl-certificates) |
| [Delete Database](actions/delete-database.md) | `DELETE /stacks/:stack_id/server_groups/:server_group_id/databases/:id` | [docs](https://developers.cloud66.com/v3/endpoints/databases/#delete-database) |
| [Delete Database User](actions/delete-database-user.md) | `DELETE /stacks/:stack_id/server_groups/:server_group_id/database_users/:id` | [docs](https://developers.cloud66.com/v3/endpoints/database-users/#delete-database-user) |
| [Delete Environment Variable](actions/delete-environment-variable.md) | `DELETE /stacks/:stack_id/environments/:env_var_key` | [docs](https://developers.cloud66.com/v3/endpoints/environment-variables/#delete-environment-variable) |
| [Delete SSL Certificate](actions/delete-ssl-certificate.md) | `DELETE /stacks/:stack_id/ssl_certificates/:id` | [docs](https://developers.cloud66.com/v3/endpoints/stacks/#ssl-certificates) |
| [Get Authenticated User](actions/get-authenticated-user.md) | `GET /ping/auth` | [docs](https://developers.cloud66.com/v3/endpoints/ping/#authenticated-ping) |
| [Get Deployment](actions/get-deployment.md) | `GET /stacks/:stack_id/deployments/:deployment_id` | [docs](https://developers.cloud66.com/v3/endpoints/deployments/#get-deployment) |
| [Get Environment Variable](actions/get-environment-variable.md) | `GET /stacks/:stack_id/environments/:env_var_id` | [docs](https://developers.cloud66.com/v3/endpoints/environment-variables/#get-environment-variable) |
| [Get Server](actions/get-server.md) | `GET /stacks/:stack_id/servers/:server_id` | [docs](https://developers.cloud66.com/v3/endpoints/servers/#get-server) |
| [Get SSL Certificate](actions/get-ssl-certificate.md) | `GET /stacks/:stack_id/ssl_certificates/:id` | [docs](https://developers.cloud66.com/v3/endpoints/stacks/#ssl-certificates) |
| [Get Stack](actions/get-stack.md) | `GET /stacks/:id` | [docs](https://developers.cloud66.com/v3/endpoints/stacks/#get-stack) |
| [Get Stack Action](actions/get-stack-action.md) | `GET /stacks/:stack_id/actions/:id` | [docs](https://developers.cloud66.com/v3/endpoints/stacks/#get-stack-action) |
| [Get Stack Setting](actions/get-stack-setting.md) | `GET /stacks/:stack_id/settings/:id` | [docs](https://developers.cloud66.com/v3/endpoints/stack-settings/#get-stack-setting) |
| [Import Backup](actions/import-backup.md) | `POST /stacks/:stack_id/backups` | [docs](https://developers.cloud66.com/v3/endpoints/backups/#import-backup) |
| [List Backups](actions/list-backups.md) | `GET /stacks/:id/backups` | [docs](https://developers.cloud66.com/v3/endpoints/backups/#list-backups) |
| [List Database Users](actions/list-database-users.md) | `GET /stacks/:stack_id/server_groups/:server_group_id/database_users` | [docs](https://developers.cloud66.com/v3/endpoints/database-users/#list-database-users) |
| [List Databases](actions/list-databases.md) | `GET /stacks/:stack_id/server_groups/:server_group_id/databases` | [docs](https://developers.cloud66.com/v3/endpoints/databases/#list-databases) |
| [List Deployments](actions/list-deployments.md) | `GET /stacks/:stack_id/deployments` | [docs](https://developers.cloud66.com/v3/endpoints/deployments/#list-deployments) |
| [List Environment Variables](actions/list-environment-variables.md) | `GET /stacks/:stack_id/environments` | [docs](https://developers.cloud66.com/v3/endpoints/environment-variables/#list-environment-variables) |
| [List Jobs](actions/list-jobs.md) | `GET /stacks/:stack_id/jobs` | [docs](https://developers.cloud66.com/v3/endpoints/jobs/#list-jobs) |
| [List Processes](actions/list-processes.md) | `GET /stacks/:stack_id/processes` | [docs](https://developers.cloud66.com/v3/endpoints/processes/#list-processes) |
| [List Server Groups](actions/list-server-groups.md) | `GET /stacks/:stack_id/server_groups` | [docs](https://developers.cloud66.com/v3/endpoints/server-groups/#list-server-groups) |
| [List Servers](actions/list-servers.md) | `GET /stacks/:stack_id/servers` | [docs](https://developers.cloud66.com/v3/endpoints/servers/#list-servers) |
| [List Services](actions/list-services.md) | `GET /stacks/:stack_id/services` | [docs](https://developers.cloud66.com/v3/endpoints/services/#list-services) |
| [List SSL Certificates](actions/list-ssl-certificates.md) | `GET /stacks/:stack_id/ssl_certificates` | [docs](https://developers.cloud66.com/v3/endpoints/stacks/#ssl-certificates) |
| [List Stack Actions](actions/list-stack-actions.md) | `GET /stacks/:id/actions` | [docs](https://developers.cloud66.com/v3/endpoints/stacks/#stack-actions-list) |
| [List Stack Settings](actions/list-stack-settings.md) | `GET /stacks/:stack_id/settings` | [docs](https://developers.cloud66.com/v3/endpoints/stack-settings/#list-stack-settings) |
| [List Stacks](actions/list-stacks.md) | `GET /stacks` | [docs](https://developers.cloud66.com/v3/endpoints/stacks/#list-stacks) |
| [Reboot Server](actions/reboot-server.md) | `POST /stacks/:stack_id/servers/:server_id/reboot` | [docs](https://developers.cloud66.com/v3/endpoints/servers/#reboot-server) |
| [Redeploy Stack](actions/redeploy-stack.md) | `POST /stacks/:stack_id/deployments` | [docs](https://developers.cloud66.com/v3/endpoints/deployments/#redeploy-stack) |
| [Regenerate Database User Password](actions/regenerate-database-user-password.md) | `POST /stacks/:stack_id/server_groups/:server_group_id/database_users/:id/regenerate_password` | [docs](https://developers.cloud66.com/v3/endpoints/database-users/#regenerate-database-user-password) |
| [Scale Process](actions/scale-process.md) | `POST /stacks/:stack_id/processes/:id/scale` | [docs](https://developers.cloud66.com/v3/endpoints/processes/#scale-process) |
| [Update Environment Variable](actions/update-environment-variable.md) | `PUT /stacks/:stack_id/environments/:env_var_key` | [docs](https://developers.cloud66.com/v3/endpoints/environment-variables/#update-environment-variable) |
| [Update SSL Certificate](actions/update-ssl-certificate.md) | `PATCH /stacks/:stack_id/ssl_certificates/:id` | [docs](https://developers.cloud66.com/v3/endpoints/stacks/#ssl-certificates) |
| [Update Stack Setting](actions/update-stack-setting.md) | `PUT /stacks/:stack_id/settings/:id` | [docs](https://developers.cloud66.com/v3/endpoints/stack-settings/#update-stack-setting) |
