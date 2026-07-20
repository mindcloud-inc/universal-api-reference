# <img src="https://images.mindcloud.co/apps/icons/56da639b-d03a-4800-b4d4-e42dc86af7c8_1776287391790.png" alt="Elastic Cloud logo" width="28" height="28"> Elastic Cloud: Universal API

Manage Elastic Cloud deployments, templates, extensions, and traffic filters

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/elasticCloud/latest
- **Category:** IT Operations / DevOps
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.elastic.co/cloud
- **Vendor API docs:** https://www.elastic.co/docs/api/doc/cloud/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Deployments](actions/list-deployments.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/list-deployments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Certificate Authority

| Action | Method | Description |
| --- | --- | --- |
| [Get Deployment Certificate Authority](actions/get-deployment-certificate-authority.md) | GET | Retrieves a deployment certificate authority from Elastic Cloud. |

### Deployment

| Action | Method | Description |
| --- | --- | --- |
| [Create Deployment](actions/create-deployment.md) | POST | Creates a new deployment in Elastic Cloud. |
| [Get Deployment](actions/get-deployment.md) | GET | Retrieves a deployment from Elastic Cloud. |
| [List Deployments](actions/list-deployments.md) | GET | Retrieves deployments from Elastic Cloud. |
| [Restore Deployment](actions/restore-deployment.md) | PUT | Restores a shutdown deployment in Elastic Cloud. |
| [Search Deployments](actions/search-deployments.md) | GET | Finds deployments in Elastic Cloud by query. |
| [Shut Down Deployment](actions/shutdown-deployment.md) | PUT | Shuts down a deployment in Elastic Cloud. |
| [Update Deployment](actions/update-deployment.md) | PUT | Updates an existing deployment in Elastic Cloud. |

### Deployment Tag

| Action | Method | Description |
| --- | --- | --- |
| [Get Deployment Tags](actions/get-deployment-tags.md) | GET | Retrieves deployment tags from Elastic Cloud. |
| [Set Deployment Tags](actions/set-deployment-tags.md) | PUT | Updates deployment tags in Elastic Cloud. |

### Deployment Template

| Action | Method | Description |
| --- | --- | --- |
| [Get Deployment Template](actions/get-deployment-template.md) | GET | Retrieves a deployment template from Elastic Cloud. |
| [List Deployment Templates](actions/list-deployment-templates.md) | GET | Retrieves deployment templates from Elastic Cloud. |

### Extension

| Action | Method | Description |
| --- | --- | --- |
| [Create Extension](actions/create-extension.md) | POST | Creates a new extension in Elastic Cloud. |
| [Delete Extension](actions/delete-extension.md) | DELETE | Deletes an existing extension from Elastic Cloud. |
| [Get Extension](actions/get-extension.md) | GET | Retrieves an extension from Elastic Cloud. |
| [List Extensions](actions/list-extensions.md) | GET | Retrieves extensions from Elastic Cloud. |
| [Update Extension](actions/update-extension.md) | PUT | Updates an existing extension in Elastic Cloud. |
| [Upload Extension](actions/upload-extension.md) | PUT | Uploads an extension archive to Elastic Cloud. |

### Traffic Filter Ruleset

| Action | Method | Description |
| --- | --- | --- |
| [Create Traffic Filter Ruleset](actions/create-traffic-filter-ruleset.md) | POST | Creates a new traffic filter ruleset in Elastic Cloud. |
| [Delete Traffic Filter Ruleset](actions/delete-traffic-filter-ruleset.md) | DELETE | Deletes an existing traffic filter ruleset from Elastic Cloud. |
| [Get Traffic Filter Ruleset](actions/get-traffic-filter-ruleset.md) | GET | Retrieves a traffic filter ruleset from Elastic Cloud. |
| [List Traffic Filter Rulesets](actions/list-traffic-filter-rulesets.md) | GET | Retrieves traffic filter rulesets from Elastic Cloud. |
| [Update Traffic Filter Ruleset](actions/update-traffic-filter-ruleset.md) | PUT | Updates an existing traffic filter ruleset in Elastic Cloud. |

### Upgrade Assistant Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Deployment Upgrade Assistant Status](actions/get-deployment-upgrade-assistant-status.md) | GET | Retrieves deployment upgrade assistant status from Elastic Cloud. |

