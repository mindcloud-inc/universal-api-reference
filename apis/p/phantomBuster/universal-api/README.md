# <img src="https://images.mindcloud.co/apps/icons/phantom-buster_1773691764542.png" alt="PhantomBuster logo" width="28" height="28"> PhantomBuster: Universal API

Launch agents, manage scripts, and access PhantomBuster data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/phantomBuster/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://phantombuster.com
- **Vendor API docs:** https://hub.phantombuster.com/docs/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Branches](actions/list-branches.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/list-branches?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Agent

| Action | Method | Description |
| --- | --- | --- |
| [Delete Agent](actions/delete-agent.md) | DELETE | Deletes an agent from PhantomBuster. |
| [Get Agent](actions/get-agent.md) | GET | Retrieves an agent from PhantomBuster. |
| [List Agents](actions/list-agents.md) | GET | Retrieves agents from PhantomBuster. |
| [List Deleted Agents](actions/list-deleted-agents.md) | GET | Retrieves deleted agents from PhantomBuster. |
| [Save Agent](actions/save-agent.md) | PUT | Updates an agent in PhantomBuster. |
| [Stop Agent](actions/stop-agent.md) | PUT | Stops a running agent in PhantomBuster. |

### Agentgroup

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization Agent Groups](actions/get-organization-agent-groups.md) | GET | Retrieves organization agent groups from PhantomBuster. |

### Agentlaunch

| Action | Method | Description |
| --- | --- | --- |
| [Launch Agent](actions/launch-agent.md) | POST | Launches an agent in PhantomBuster. |
| [Schedule Agent Launch](actions/schedule-agent-launch.md) | POST | Schedules an agent launch in PhantomBuster. |

### Agentoutput

| Action | Method | Description |
| --- | --- | --- |
| [Get Agent Output](actions/get-agent-output.md) | GET | Retrieves agent output from PhantomBuster. |

### Branch

| Action | Method | Description |
| --- | --- | --- |
| [Compare Branches](actions/compare-branches.md) | GET | Retrieves differences between branches in PhantomBuster. |
| [List Branches](actions/list-branches.md) | GET | Retrieves branches from PhantomBuster. |

### Container

| Action | Method | Description |
| --- | --- | --- |
| [Get Container](actions/get-container.md) | GET | Retrieves a container from PhantomBuster. |
| [List Containers](actions/list-containers.md) | GET | Retrieves containers from PhantomBuster. |
| [List Running Containers](actions/list-running-containers.md) | GET | Retrieves running containers from PhantomBuster. |

### Containeroutput

| Action | Method | Description |
| --- | --- | --- |
| [Get Container Output](actions/get-container-output.md) | GET | Retrieves container output from PhantomBuster. |

### Crmaccess

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization CRM Access](actions/get-organization-crm-access.md) | GET | Retrieves organization CRM access from PhantomBuster. |

### Crmresource

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization CRM Resources](actions/get-organization-crm-resources.md) | GET | Retrieves organization CRM resources from PhantomBuster. |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [Get IP Location](actions/get-ip-location.md) | GET | Retrieves IP location details from PhantomBuster. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization](actions/get-organization.md) | GET | Retrieves organization details from PhantomBuster. |

### Organizationresource

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization Resources](actions/get-organization-resources.md) | GET | Retrieves organization resources from PhantomBuster. |

### Script

| Action | Method | Description |
| --- | --- | --- |
| [Get Script](actions/get-script.md) | GET | Retrieves a script from PhantomBuster. |
| [List Scripts](actions/list-scripts.md) | GET | Retrieves scripts from PhantomBuster. |

### Scriptcode

| Action | Method | Description |
| --- | --- | --- |
| [Get Script Code](actions/get-script-code.md) | GET | Retrieves script code from PhantomBuster. |

