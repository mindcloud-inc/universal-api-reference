# Elastic Cloud: Native API Reference

A consolidated summary of Elastic Cloud's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://www.elastic.co/docs/api/doc/cloud/
- **OpenAPI specification:** https://api.elastic-cloud.com/api/v1/api-docs-user/swagger.json
- **API base URL:** `https://api.elastic-cloud.com/api/v1`

## Authentication

### API Key

Connect with an Elastic Cloud API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.elastic.co/docs/api/doc/cloud/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Deployment](actions/create-deployment.md) | `POST /deployments` | [docs](https://www.elastic.co/docs/api/doc/cloud/operation/operation-create-deployment) |
| [Create Extension](actions/create-extension.md) | `POST /deployments/extensions` | [docs](https://www.elastic.co/docs/api/doc/cloud/operation/operation-create-extension) |
| [Create Traffic Filter Ruleset](actions/create-traffic-filter-ruleset.md) | `POST /deployments/traffic-filter/rulesets` | [docs](https://www.elastic.co/docs/api/doc/cloud/operation/operation-create-traffic-filter-ruleset) |
| [Delete Extension](actions/delete-extension.md) | `DELETE /deployments/extensions/:extension_id` | [docs](https://www.elastic.co/docs/api/doc/cloud/operation/operation-delete-extension) |
| [Delete Traffic Filter Ruleset](actions/delete-traffic-filter-ruleset.md) | `DELETE /deployments/traffic-filter/rulesets/:ruleset_id` | [docs](https://www.elastic.co/docs/api/doc/cloud/operation/operation-delete-traffic-filter-ruleset) |
| [Get Deployment](actions/get-deployment.md) | `GET /deployments/:deployment_id` | [docs](https://www.elastic.co/docs/api/doc/cloud/operation/operation-get-deployment) |
| [Get Deployment Certificate Authority](actions/get-deployment-certificate-authority.md) | `GET /deployments/:deployment_id/certificate-authority` | [docs](https://www.elastic.co/docs/api/doc/cloud/operation/operation-get-deployment-certificate-authority) |
| [Get Deployment Tags](actions/get-deployment-tags.md) | `GET /deployments/:deployment_id/tags` | [docs](https://www.elastic.co/docs/api/doc/cloud/operation/operation-get-deployment-tags) |
| [Get Deployment Template](actions/get-deployment-template.md) | `GET /deployments/templates/:template_id` | [docs](https://www.elastic.co/docs/api/doc/cloud/operation/operation-get-deployment-template-v2) |
| [Get Deployment Upgrade Assistant Status](actions/get-deployment-upgrade-assistant-status.md) | `GET /deployments/:deployment_id/upgrade_assistant/status` | [docs](https://www.elastic.co/docs/api/doc/cloud/operation/operation-get-deployment-upgrade-assistant-status) |
| [Get Extension](actions/get-extension.md) | `GET /deployments/extensions/:extension_id` | [docs](https://www.elastic.co/docs/api/doc/cloud/operation/operation-get-extension) |
| [Get Traffic Filter Ruleset](actions/get-traffic-filter-ruleset.md) | `GET /deployments/traffic-filter/rulesets/:ruleset_id` | [docs](https://www.elastic.co/docs/api/doc/cloud/operation/operation-get-traffic-filter-ruleset) |
| [List Deployment Templates](actions/list-deployment-templates.md) | `GET /deployments/templates` | [docs](https://www.elastic.co/docs/api/doc/cloud/operation/operation-get-deployment-templates-v2) |
| [List Deployments](actions/list-deployments.md) | `GET /deployments` | [docs](https://www.elastic.co/docs/api/doc/cloud/operation/operation-list-deployments) |
| [List Extensions](actions/list-extensions.md) | `GET /deployments/extensions` | [docs](https://www.elastic.co/docs/api/doc/cloud/operation/operation-list-extensions) |
| [List Traffic Filter Rulesets](actions/list-traffic-filter-rulesets.md) | `GET /deployments/traffic-filter/rulesets` | [docs](https://www.elastic.co/docs/api/doc/cloud/operation/operation-get-traffic-filter-rulesets) |
| [Restore Deployment](actions/restore-deployment.md) | `POST /deployments/:deployment_id/_restore` | [docs](https://www.elastic.co/docs/api/doc/cloud/operation/operation-restore-deployment) |
| [Search Deployments](actions/search-deployments.md) | `POST /deployments/_search` | [docs](https://www.elastic.co/docs/api/doc/cloud/operation/operation-search-deployments) |
| [Set Deployment Tags](actions/set-deployment-tags.md) | `PUT /deployments/:deployment_id/tags` | [docs](https://www.elastic.co/docs/api/doc/cloud/operation/operation-set-deployment-tags) |
| [Shut Down Deployment](actions/shutdown-deployment.md) | `POST /deployments/:deployment_id/_shutdown` | [docs](https://www.elastic.co/docs/api/doc/cloud/operation/operation-shutdown-deployment) |
| [Update Deployment](actions/update-deployment.md) | `PUT /deployments/:deployment_id` | [docs](https://www.elastic.co/docs/api/doc/cloud/operation/operation-update-deployment) |
| [Update Extension](actions/update-extension.md) | `POST /deployments/extensions/:extension_id` | [docs](https://www.elastic.co/docs/api/doc/cloud/operation/operation-update-extension) |
| [Update Traffic Filter Ruleset](actions/update-traffic-filter-ruleset.md) | `PUT /deployments/traffic-filter/rulesets/:ruleset_id` | [docs](https://www.elastic.co/docs/api/doc/cloud/operation/operation-update-traffic-filter-ruleset) |
| [Upload Extension](actions/upload-extension.md) | `PUT /deployments/extensions/:extension_id` | [docs](https://www.elastic.co/docs/api/doc/cloud/operation/operation-upload-extension) |
