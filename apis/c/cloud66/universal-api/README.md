# <img src="https://images.mindcloud.co/apps/icons/cloud66_1775071063641.png" alt="Cloud 66 logo" width="28" height="28"> Cloud 66: Universal API

Deploy, manage, and scale applications on your own servers

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cloud66/latest
- **Category:** IT Operations / DevOps
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.cloud66.com
- **Vendor API docs:** https://developers.cloud66.com/v3/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Authenticated User](actions/get-authenticated-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloud66/latest/actions/get-authenticated-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Authenticated User

| Action | Method | Description |
| --- | --- | --- |
| [Get Authenticated User](actions/get-authenticated-user.md) | GET | Retrieves the authenticated user from your Cloud 66 account. |

### Database

| Action | Method | Description |
| --- | --- | --- |
| [Create Database](actions/create-database.md) | POST | Creates a database in your Cloud 66 account. |
| [Delete Database](actions/delete-database.md) | DELETE | Deletes a database from your Cloud 66 account. |
| [List Databases](actions/list-databases.md) | GET | Retrieves databases from your Cloud 66 account. |

### Database User

| Action | Method | Description |
| --- | --- | --- |
| [Create Database User](actions/create-database-user.md) | POST | Creates a database user in your Cloud 66 account. |
| [Delete Database User](actions/delete-database-user.md) | DELETE | Deletes a database user from your Cloud 66 account. |
| [List Database Users](actions/list-database-users.md) | GET | Retrieves database users from your Cloud 66 account. |
| [Regenerate Database User Password](actions/regenerate-database-user-password.md) | PUT | Regenerates a database user password in Cloud 66. |

### Environment Variable

| Action | Method | Description |
| --- | --- | --- |
| [Add Environment Variable](actions/add-environment-variable.md) | POST | Creates an environment variable in your Cloud 66 account. |
| [Delete Environment Variable](actions/delete-environment-variable.md) | DELETE | Deletes an environment variable from your Cloud 66 account. |
| [Get Environment Variable](actions/get-environment-variable.md) | GET | Retrieves an environment variable from your Cloud 66 account. |
| [List Environment Variables](actions/list-environment-variables.md) | GET | Retrieves environment variables from your Cloud 66 account. |
| [Update Environment Variable](actions/update-environment-variable.md) | PUT | Updates an environment variable in your Cloud 66 account. |

### Services

| Action | Method | Description |
| --- | --- | --- |
| [List Services](actions/list-services.md) | GET | Retrieves services from your Cloud 66 account. |

### Ssl Certificate

| Action | Method | Description |
| --- | --- | --- |
| [Create SSL Certificate](actions/create-ssl-certificate.md) | POST | Creates an SSL certificate in your Cloud 66 account. |
| [Delete SSL Certificate](actions/delete-ssl-certificate.md) | DELETE | Deletes an SSL certificate from your Cloud 66 account. |
| [Get SSL Certificate](actions/get-ssl-certificate.md) | GET | Retrieves an SSL certificate from your Cloud 66 account. |
| [List SSL Certificates](actions/list-ssl-certificates.md) | GET | Retrieves SSL certificates from your Cloud 66 account. |
| [Update SSL Certificate](actions/update-ssl-certificate.md) | PUT | Updates an SSL certificate in your Cloud 66 account. |

### Stack Setting

| Action | Method | Description |
| --- | --- | --- |
| [Get Stack Setting](actions/get-stack-setting.md) | GET | Retrieves a stack setting from your Cloud 66 account. |
| [List Stack Settings](actions/list-stack-settings.md) | GET | Retrieves stack settings from your Cloud 66 account. |
| [Update Stack Setting](actions/update-stack-setting.md) | PUT | Updates a stack setting in your Cloud 66 account. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [List Jobs](actions/list-jobs.md) | GET | Retrieves jobs from your Cloud 66 account. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Deployment](actions/cancel-deployment.md) | DELETE | Cancels a deployment in your Cloud 66 account. |
| [Create Backup](actions/create-backup.md) | POST | Creates a backup for a Cloud 66 stack. |
| [Get Deployment](actions/get-deployment.md) | GET | Retrieves a deployment from your Cloud 66 account. |
| [Get Server](actions/get-server.md) | GET | Retrieves a server from your Cloud 66 account. |
| [Get Stack](actions/get-stack.md) | GET | Retrieves a stack from your Cloud 66 account. |
| [Get Stack Action](actions/get-stack-action.md) | GET | Retrieves a stack action from your Cloud 66 account. |
| [Import Backup](actions/import-backup.md) | POST | Imports a backup into a Cloud 66 stack. |
| [List Backups](actions/list-backups.md) | GET | Retrieves backups from your Cloud 66 account. |
| [List Deployments](actions/list-deployments.md) | GET | Retrieves deployments from your Cloud 66 account. |
| [List Processes](actions/list-processes.md) | GET | Retrieves processes from your Cloud 66 account. |
| [List Server Groups](actions/list-server-groups.md) | GET | Retrieves server groups from your Cloud 66 account. |
| [List Servers](actions/list-servers.md) | GET | Retrieves servers from your Cloud 66 account. |
| [List Stack Actions](actions/list-stack-actions.md) | GET | Retrieves stack actions from your Cloud 66 account. |
| [List Stacks](actions/list-stacks.md) | GET | Retrieves stacks from your Cloud 66 account. |
| [Reboot Server](actions/reboot-server.md) | PUT | Reboots a server in your Cloud 66 account. |
| [Redeploy Stack](actions/redeploy-stack.md) | POST | Redeploys a stack in your Cloud 66 account. |
| [Scale Process](actions/scale-process.md) | PUT | Scales a process in your Cloud 66 account. |

