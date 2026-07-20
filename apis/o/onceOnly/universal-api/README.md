# <img src="https://images.mindcloud.co/apps/icons/images-1_1775062225384.png" alt="OnceOnly logo" width="28" height="28"> OnceOnly: Universal API

OnceOnly is an execution-safety and governance API for idempotency checks, AI leases, run events, tools, policies, and agent controls.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/onceOnly/latest
- **Category:** IT Operations / Security & Compliance
- **Actions:** 28
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://onceonly.tech/
- **Vendor API docs:** https://docs.onceonly.tech/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Usage](actions/get-usage.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onceOnly/latest/actions/get-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (28)

### Agent

| Action | Method | Description |
| --- | --- | --- |
| [Disable Agent](actions/disable-agent.md) | PUT | Disables an agent in OnceOnly. |
| [Enable Agent](actions/enable-agent.md) | PUT | Enables an agent in OnceOnly. |
| [Get Agent Metrics](actions/get-agent-metrics.md) | GET | Retrieves agent metrics from OnceOnly. |
| [List Agent Logs](actions/list-agent-logs.md) | GET | Retrieves agent logs from OnceOnly. |

### Ai Lease

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Lease](actions/cancel-lease.md) | PUT | Cancels an AI lease in OnceOnly. |
| [Check Status](actions/check-status.md) | GET | Retrieves AI lease status from OnceOnly. |
| [Complete Lease](actions/complete-lease.md) | PUT | Completes an AI lease in OnceOnly. |
| [Create Lease](actions/create-lease.md) | POST | Creates an AI lease in OnceOnly. |
| [Extend Lease](actions/extend-lease.md) | PUT | Extends an AI lease in OnceOnly. |
| [Fail Lease](actions/fail-lease.md) | PUT | Marks an AI lease as failed in OnceOnly. |

### Ai Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Result](actions/get-result.md) | GET | Retrieves an AI task result from OnceOnly. |

### Ai Run

| Action | Method | Description |
| --- | --- | --- |
| [Run AI Task](actions/run-ai-task.md) | POST | Runs an AI task in OnceOnly. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Create Run Event](actions/create-run-event.md) | POST | Creates a run event in OnceOnly. |
| [List Recent Namespace Events](actions/list-recent-namespace-events.md) | GET | Retrieves recent namespace events from OnceOnly. |

### Lock

| Action | Method | Description |
| --- | --- | --- |
| [Check Lock](actions/check-lock.md) | POST | Checks an idempotency lock in OnceOnly. |

### Policy

| Action | Method | Description |
| --- | --- | --- |
| [Create or Update Policy](actions/create-or-update-policy.md) | PUT | Creates or updates a policy in OnceOnly. |
| [Create Policy From Template](actions/create-policy-from-template.md) | POST | Creates a policy from a template in OnceOnly. |
| [Get Policy](actions/get-policy.md) | GET | Retrieves a policy from OnceOnly. |
| [List Policies](actions/list-policies.md) | GET | Retrieves policies from OnceOnly. |

### Run

| Action | Method | Description |
| --- | --- | --- |
| [Get Run Timeline](actions/get-run-timeline.md) | GET | Retrieves a run timeline from OnceOnly. |
| [List Runs](actions/list-runs.md) | GET | Retrieves runs from OnceOnly. |

### Tool

| Action | Method | Description |
| --- | --- | --- |
| [Create or Update Tool](actions/create-or-update-tool.md) | POST | Creates or updates a tool in OnceOnly. |
| [Delete Tool](actions/delete-tool.md) | DELETE | Deletes a tool from OnceOnly. |
| [Get Tool](actions/get-tool.md) | GET | Retrieves a tool from OnceOnly. |
| [List Tools](actions/list-tools.md) | GET | Retrieves tools from OnceOnly. |
| [Toggle Tool](actions/toggle-tool.md) | PUT | Updates a tool's enabled status in OnceOnly. |

### Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Usage](actions/get-usage.md) | GET | Retrieves usage details from OnceOnly. |
| [Get Usage For All Kinds](actions/get-usage-for-all-kinds.md) | GET | Retrieves usage details for all kinds from OnceOnly. |

