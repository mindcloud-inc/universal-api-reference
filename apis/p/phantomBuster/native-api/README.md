# PhantomBuster: Native API Reference

A consolidated summary of PhantomBuster's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://hub.phantombuster.com/docs/api
- **API base URL:** `https://api.phantombuster.com/api/v2`

## Authentication

### API Key

Use your PhantomBuster API key to access the V2 API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-Phantombuster-Key: <apiKey>
```

[Official authentication documentation](https://hub.phantombuster.com/reference/buster-apikey)

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
| [Compare Branches](actions/compare-branches.md) | `GET /branches/diff` | [docs](https://hub.phantombuster.com/reference/get_branches-diff) |
| [Delete Agent](actions/delete-agent.md) | `POST /agents/delete` | [docs](https://hub.phantombuster.com/reference/post_agents-delete) |
| [Get Agent](actions/get-agent.md) | `GET /agents/fetch` | [docs](https://hub.phantombuster.com/reference/get_agents-fetch) |
| [Get Agent Output](actions/get-agent-output.md) | `GET /agents/fetch-output` | [docs](https://hub.phantombuster.com/reference/get_agents-fetch-output) |
| [Get Container](actions/get-container.md) | `GET /containers/fetch` | [docs](https://hub.phantombuster.com/reference/get_containers-fetch) |
| [Get Container Output](actions/get-container-output.md) | `GET /containers/fetch-output` | [docs](https://hub.phantombuster.com/reference/get_containers-fetch-output) |
| [Get IP Location](actions/get-ip-location.md) | `GET /location/ip` | [docs](https://hub.phantombuster.com/reference/get_location-ip) |
| [Get Organization](actions/get-organization.md) | `GET /orgs/fetch` | [docs](https://hub.phantombuster.com/reference/get_orgs-fetch) |
| [Get Organization Agent Groups](actions/get-organization-agent-groups.md) | `GET /orgs/fetch-agent-groups` | [docs](https://hub.phantombuster.com/reference/get_orgs-fetch-agent-groups) |
| [Get Organization CRM Access](actions/get-organization-crm-access.md) | `GET /orgs/fetch-crm-access` | [docs](https://hub.phantombuster.com/reference/get_orgs-fetch-crm-access) |
| [Get Organization CRM Resources](actions/get-organization-crm-resources.md) | `GET /orgs/fetch-crm-resources` | [docs](https://hub.phantombuster.com/reference/get_orgs-fetch-crm-resources) |
| [Get Organization Resources](actions/get-organization-resources.md) | `GET /orgs/fetch-resources` | [docs](https://hub.phantombuster.com/reference/get_orgs-fetch-resources) |
| [Get Script](actions/get-script.md) | `GET /scripts/fetch` | [docs](https://hub.phantombuster.com/reference/get_scripts-fetch) |
| [Get Script Code](actions/get-script-code.md) | `GET /scripts/code` | [docs](https://hub.phantombuster.com/reference/get_scripts-code) |
| [Launch Agent](actions/launch-agent.md) | `POST /agents/launch` | [docs](https://hub.phantombuster.com/reference/post_agents-launch) |
| [List Agents](actions/list-agents.md) | `GET /agents/fetch-all` | [docs](https://hub.phantombuster.com/reference/get_agents-fetch-all) |
| [List Branches](actions/list-branches.md) | `GET /branches/fetch-all` | [docs](https://hub.phantombuster.com/reference/get_branches-fetch-all) |
| [List Containers](actions/list-containers.md) | `GET /containers/fetch-all` | [docs](https://hub.phantombuster.com/reference/get_containers-fetch-all) |
| [List Deleted Agents](actions/list-deleted-agents.md) | `GET /agents/fetch-deleted` | [docs](https://hub.phantombuster.com/reference/get_agents-fetch-deleted) |
| [List Running Containers](actions/list-running-containers.md) | `GET /orgs/fetch-running-containers` | [docs](https://hub.phantombuster.com/reference/get_orgs-fetch-running-containers) |
| [List Scripts](actions/list-scripts.md) | `GET /scripts/fetch-all` | [docs](https://hub.phantombuster.com/reference/get_scripts-fetch-all) |
| [Save Agent](actions/save-agent.md) | `POST /agents/save` | [docs](https://hub.phantombuster.com/reference/post_agents-save) |
| [Schedule Agent Launch](actions/schedule-agent-launch.md) | `POST /agents/launch-soon` | [docs](https://hub.phantombuster.com/reference/post_agents-launch-soon) |
| [Stop Agent](actions/stop-agent.md) | `POST /agents/stop` | [docs](https://hub.phantombuster.com/reference/post_agents-stop) |
