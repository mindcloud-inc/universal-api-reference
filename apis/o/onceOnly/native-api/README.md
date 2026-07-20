# OnceOnly: Native API Reference

A consolidated summary of OnceOnly's API configuration and 28 documented operations, with links to official documentation.

- **Official docs:** https://docs.onceonly.tech/
- **API base URL:** `https://api.onceonly.tech`

## Authentication

### API Key

Use a OnceOnly API key sent as an Authorization bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.onceonly.tech/start-here/quickstart/)

## Endpoints (28 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Lease](actions/cancel-lease.md) | `POST /v1/ai/cancel` | [docs](https://docs.onceonly.tech/reference/ai/) |
| [Check Lock](actions/check-lock.md) | `POST /v1/check-lock` | [docs](https://docs.onceonly.tech/reference/idempotency/) |
| [Check Status](actions/check-status.md) | `GET /v1/ai/status` | [docs](https://docs.onceonly.tech/reference/ai/) |
| [Complete Lease](actions/complete-lease.md) | `POST /v1/ai/complete` | [docs](https://docs.onceonly.tech/reference/ai/) |
| [Create Lease](actions/create-lease.md) | `POST /v1/ai/lease` | [docs](https://docs.onceonly.tech/reference/ai/) |
| [Create or Update Policy](actions/create-or-update-policy.md) | `POST /v1/policies/:agent_id` | [docs](https://docs.onceonly.tech/reference/policies/) |
| [Create or Update Tool](actions/create-or-update-tool.md) | `POST /v1/tools` | [docs](https://docs.onceonly.tech/reference/tools/) |
| [Create Policy From Template](actions/create-policy-from-template.md) | `POST /v1/policies/:agent_id/from-template` | [docs](https://docs.onceonly.tech/reference/policies/) |
| [Create Run Event](actions/create-run-event.md) | `POST /v1/events` | [docs](https://docs.onceonly.tech/reference/runs/) |
| [Delete Tool](actions/delete-tool.md) | `DELETE /v1/tools/:name` | [docs](https://docs.onceonly.tech/reference/tools/) |
| [Disable Agent](actions/disable-agent.md) | `POST /v1/agents/:agent_id/disable` | [docs](https://docs.onceonly.tech/reference/agents/) |
| [Enable Agent](actions/enable-agent.md) | `POST /v1/agents/:agent_id/enable` | [docs](https://docs.onceonly.tech/reference/agents/) |
| [Extend Lease](actions/extend-lease.md) | `POST /v1/ai/extend` | [docs](https://docs.onceonly.tech/reference/ai/) |
| [Fail Lease](actions/fail-lease.md) | `POST /v1/ai/fail` | [docs](https://docs.onceonly.tech/reference/ai/) |
| [Get Agent Metrics](actions/get-agent-metrics.md) | `GET /v1/agents/:agent_id/metrics` | [docs](https://docs.onceonly.tech/reference/agents/) |
| [Get Policy](actions/get-policy.md) | `GET /v1/policies/:agent_id` | [docs](https://docs.onceonly.tech/reference/policies/) |
| [Get Result](actions/get-result.md) | `GET /v1/ai/result` | [docs](https://docs.onceonly.tech/reference/ai/) |
| [Get Run Timeline](actions/get-run-timeline.md) | `GET /v1/runs/:run_id` | [docs](https://docs.onceonly.tech/reference/runs/) |
| [Get Tool](actions/get-tool.md) | `GET /v1/tools/:name` | [docs](https://docs.onceonly.tech/reference/tools/) |
| [Get Usage](actions/get-usage.md) | `GET /v1/usage` | [docs](https://docs.onceonly.tech/reference/usage/) |
| [Get Usage For All Kinds](actions/get-usage-for-all-kinds.md) | `GET /v1/usage/all` | [docs](https://docs.onceonly.tech/reference/usage/) |
| [List Agent Logs](actions/list-agent-logs.md) | `GET /v1/agents/:agent_id/logs` | [docs](https://docs.onceonly.tech/reference/agents/) |
| [List Policies](actions/list-policies.md) | `GET /v1/policies` | [docs](https://docs.onceonly.tech/reference/policies/) |
| [List Recent Namespace Events](actions/list-recent-namespace-events.md) | `GET /v1/events` | [docs](https://docs.onceonly.tech/reference/runs/) |
| [List Runs](actions/list-runs.md) | `GET /v1/runs` | [docs](https://docs.onceonly.tech/reference/runs/) |
| [List Tools](actions/list-tools.md) | `GET /v1/tools` | [docs](https://docs.onceonly.tech/reference/tools/) |
| [Run AI Task](actions/run-ai-task.md) | `POST /v1/ai/run` | [docs](https://docs.onceonly.tech/reference/ai-run/) |
| [Toggle Tool](actions/toggle-tool.md) | `POST /v1/tools/:name/toggle` | [docs](https://docs.onceonly.tech/reference/tools/) |
