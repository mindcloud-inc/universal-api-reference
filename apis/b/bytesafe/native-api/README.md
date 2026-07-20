# Bytesafe: Native API Reference

A consolidated summary of Bytesafe's API configuration and 31 documented operations.

- **API base URL:** `https://mindcloud.bytesafe.dev/api/v1/`

## Authentication

### API Key

Authenticate with a Bytesafe API token sent as a bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.bytesafe.dev/account-and-profile/managing-tokens/)

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Advisory](actions/get-advisory.md) | `GET /artifacts/advisory/:advisoryId` | [docs](https://docs.bytesafe.dev/issues/) |
| [Get Authenticated User](actions/get-authenticated-user.md) | `GET /whoami` | [docs](https://docs.bytesafe.dev/account-and-profile/profile/) |
| [Get GitHub Integration Status](actions/get-git-hub-integration-status.md) | `GET /integrations/github/status` | [docs](https://docs.bytesafe.dev/integrations/github/) |
| [Get Issue](actions/get-issue.md) | `GET /issues/:issueId` | [docs](https://docs.bytesafe.dev/issues/) |
| [Get Issue Count](actions/get-issue-count.md) | `GET /issues/count` | [docs](https://docs.bytesafe.dev/reports/issues-summary/) |
| [Get License](actions/get-license.md) | `GET /licenses/:licenseKey` | [docs](https://docs.bytesafe.dev/working-with-registries/package-licenses/) |
| [Get License Policy](actions/get-license-policy.md) | `GET /license-policies/:policyName` | [docs](https://docs.bytesafe.dev/license-compliance/) |
| [Get Limits](actions/get-limits.md) | `GET /limits` | [docs](https://docs.bytesafe.dev/) |
| [Get Package](actions/get-package.md) | `GET /artifacts/registries/:registryName/packages/:packageName` | [docs](https://docs.bytesafe.dev/working-with-registries/internal-packages/) |
| [Get Registry](actions/get-registry.md) | `GET /artifacts/registries/:registryId` | [docs](https://docs.bytesafe.dev/working-with-registries/) |
| [Get Registry Graph](actions/get-registry-graph.md) | `GET /artifacts/registries/:registryName/graph` | [docs](https://docs.bytesafe.dev/working-with-registries/dashboards/) |
| [Get Slack Integration Status](actions/get-slack-integration-status.md) | `GET /integrations/slack/status` | [docs](https://docs.bytesafe.dev/integrations/slack/) |
| [Get Storage Metrics](actions/get-storage-metrics.md) | `GET /metrics/storage` | [docs](https://docs.bytesafe.dev/working-with-registries/dashboards/) |
| [Get Vulnerability](actions/get-vulnerability.md) | `GET /artifacts/vulnerability/:cveId` | [docs](https://docs.bytesafe.dev/issues/) |
| [Initialize Metrics](actions/initialize-metrics.md) | `GET /metrics/initialize` | [docs](https://docs.bytesafe.dev/working-with-registries/dashboards/) |
| [List Artifact Credentials](actions/list-artifact-credentials.md) | `GET /artifacts/credentials` | [docs](https://docs.bytesafe.dev/working-with-registries/) |
| [List IAM Roles](actions/list-iam-roles.md) | `GET /iam/roles` | [docs](https://docs.bytesafe.dev/account-and-profile/iam/) |
| [List Issues](actions/list-issues.md) | `GET /issues` | [docs](https://docs.bytesafe.dev/issues/) |
| [List Latest Advisories](actions/list-latest-advisories.md) | `GET /artifacts/advisory/latest` | [docs](https://docs.bytesafe.dev/issues/) |
| [List License Policies](actions/list-license-policies.md) | `GET /license-policies` | [docs](https://docs.bytesafe.dev/license-compliance/) |
| [List Licensed Packages](actions/list-licensed-packages.md) | `GET /artifacts/registries/:registryName/licensed` | [docs](https://docs.bytesafe.dev/working-with-registries/package-licenses/) |
| [List Licenses](actions/list-licenses.md) | `GET /licenses` | [docs](https://docs.bytesafe.dev/license-compliance/) |
| [List Notifications](actions/list-notifications.md) | `GET /notifications` | [docs](https://docs.bytesafe.dev/account-and-profile/notifications/) |
| [List Package Activity](actions/list-package-activity.md) | `GET /dashboard/activity/packages` | [docs](https://docs.bytesafe.dev/working-with-registries/dashboards/) |
| [List Quarantined Packages](actions/list-quarantined-packages.md) | `GET /artifacts/registries/:registryName/quarantined` | [docs](https://docs.bytesafe.dev/quarantine/) |
| [List Registries](actions/list-registries.md) | `GET /artifacts/registries` | [docs](https://docs.bytesafe.dev/working-with-registries/) |
| [List Sessions](actions/list-sessions.md) | `GET /sessions` | [docs](https://docs.bytesafe.dev/) |
| [List Source Repositories](actions/list-source-repositories.md) | `GET /source-repositories` | [docs](https://docs.bytesafe.dev/) |
| [List Subscriptions](actions/list-subscriptions.md) | `GET /subscriptions` | [docs](https://docs.bytesafe.dev/) |
| [List Team Invites](actions/list-team-invites.md) | `GET /team/invites` | [docs](https://docs.bytesafe.dev/getting-started/invite-team-members/) |
| [List Team Members](actions/list-team-members.md) | `GET /team/members` | [docs](https://docs.bytesafe.dev/getting-started/invite-team-members/) |
