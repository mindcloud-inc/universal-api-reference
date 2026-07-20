# <img src="https://images.mindcloud.co/apps/icons/apple-touch-icon_1775059458916.png" alt="Bytesafe logo" width="28" height="28"> Bytesafe: Universal API

Bytesafe is a secure package registry and dependency firewall platform for managing internal packages, upstream sources, vulnerabilities, licenses, and team access controls.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bytesafe/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://bytesafe.dev/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Authenticated User](actions/get-authenticated-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bytesafe/latest/actions/get-authenticated-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Advisory

| Action | Method | Description |
| --- | --- | --- |
| [Get Advisory](actions/get-advisory.md) | GET | Retrieves a vulnerability advisory from Bytesafe. |
| [List Latest Advisories](actions/list-latest-advisories.md) | GET | Retrieves the latest advisories from Bytesafe. |

### Artifact Credential

| Action | Method | Description |
| --- | --- | --- |
| [List Artifact Credentials](actions/list-artifact-credentials.md) | GET |  |

### Integrations

| Action | Method | Description |
| --- | --- | --- |
| [Get GitHub Integration Status](actions/get-git-hub-integration-status.md) | GET | Retrieves GitHub integration status from Bytesafe. |
| [Get Slack Integration Status](actions/get-slack-integration-status.md) | GET | Retrieves Slack integration status from Bytesafe. |

### Invitations

| Action | Method | Description |
| --- | --- | --- |
| [List Team Invites](actions/list-team-invites.md) | GET | Retrieves team invites from your Bytesafe workspace. |

### Issue Count

| Action | Method | Description |
| --- | --- | --- |
| [Get Issue Count](actions/get-issue-count.md) | GET | Retrieves an issue count from Bytesafe reports. |

### Issues

| Action | Method | Description |
| --- | --- | --- |
| [Get Issue](actions/get-issue.md) | GET | Retrieves issue details from your Bytesafe workspace. |
| [List Issues](actions/list-issues.md) | GET | Retrieves issues from your Bytesafe workspace. |

### License

| Action | Method | Description |
| --- | --- | --- |
| [Get License](actions/get-license.md) | GET | Retrieves package license details from Bytesafe. |
| [List Licenses](actions/list-licenses.md) | GET | Retrieves package licenses from your Bytesafe workspace. |

### Licensed Package

| Action | Method | Description |
| --- | --- | --- |
| [List Licensed Packages](actions/list-licensed-packages.md) | GET | Retrieves licensed packages from a Bytesafe registry. |

### Limit

| Action | Method | Description |
| --- | --- | --- |
| [Get Limits](actions/get-limits.md) | GET |  |

### Metrics

| Action | Method | Description |
| --- | --- | --- |
| [Get Storage Metrics](actions/get-storage-metrics.md) | GET | Retrieves storage metrics from Bytesafe dashboards. |
| [Initialize Metrics](actions/initialize-metrics.md) | GET |  |

### Notifications

| Action | Method | Description |
| --- | --- | --- |
| [List Notifications](actions/list-notifications.md) | GET | Retrieves notifications from your Bytesafe account. |

### Package

| Action | Method | Description |
| --- | --- | --- |
| [Get Package](actions/get-package.md) | GET | Retrieves package details from a Bytesafe registry. |

### Package Activity

| Action | Method | Description |
| --- | --- | --- |
| [List Package Activity](actions/list-package-activity.md) | GET | Retrieves package activity from Bytesafe dashboards. |

### Policies

| Action | Method | Description |
| --- | --- | --- |
| [Get License Policy](actions/get-license-policy.md) | GET | Retrieves a license compliance policy from Bytesafe. |
| [List License Policies](actions/list-license-policies.md) | GET | Retrieves license compliance policies from Bytesafe. |

### Quarantined Package

| Action | Method | Description |
| --- | --- | --- |
| [List Quarantined Packages](actions/list-quarantined-packages.md) | GET | Retrieves quarantined packages from a Bytesafe registry. |

### Registry

| Action | Method | Description |
| --- | --- | --- |
| [Get Registry](actions/get-registry.md) | GET | Retrieves a registry from your Bytesafe workspace. |
| [List Registries](actions/list-registries.md) | GET | Retrieves registries from your Bytesafe workspace. |

### Registry Graph

| Action | Method | Description |
| --- | --- | --- |
| [Get Registry Graph](actions/get-registry-graph.md) | GET | Retrieves a registry graph from Bytesafe dashboards. |

### Repositories

| Action | Method | Description |
| --- | --- | --- |
| [List Source Repositories](actions/list-source-repositories.md) | GET |  |

### Roles

| Action | Method | Description |
| --- | --- | --- |
| [List IAM Roles](actions/list-iam-roles.md) | GET | Retrieves role-based access control roles from Bytesafe. |

### Sessions

| Action | Method | Description |
| --- | --- | --- |
| [List Sessions](actions/list-sessions.md) | GET |  |

### Subscriptions

| Action | Method | Description |
| --- | --- | --- |
| [List Subscriptions](actions/list-subscriptions.md) | GET |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Authenticated User](actions/get-authenticated-user.md) | GET | Retrieves the authenticated user from your Bytesafe workspace. |
| [List Team Members](actions/list-team-members.md) | GET | Retrieves team members from your Bytesafe workspace. |

### Vulnerabilities

| Action | Method | Description |
| --- | --- | --- |
| [Get Vulnerability](actions/get-vulnerability.md) | GET | Retrieves vulnerability details from the Bytesafe advisory database. |

