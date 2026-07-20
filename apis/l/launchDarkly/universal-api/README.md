# <img src="https://images.mindcloud.co/apps/icons/launch-darkly_1774459818715.png" alt="LaunchDarkly logo" width="28" height="28"> LaunchDarkly: Universal API

Manage LaunchDarkly flags, contexts, segments, and environments

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/launchDarkly/latest
- **Category:** IT Operations / DevOps
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://launchdarkly.com
- **Vendor API docs:** https://launchdarkly.com/docs/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Auditlogentry

| Action | Method | Description |
| --- | --- | --- |
| [List Audit Log](actions/list-audit-log.md) | GET | Retrieves audit log entries from LaunchDarkly. |

### Context

| Action | Method | Description |
| --- | --- | --- |
| [Get Context](actions/get-context.md) | GET | Retrieves a context from LaunchDarkly by kind and key. |
| [Search Contexts](actions/search-contexts.md) | GET | Finds contexts in LaunchDarkly by search criteria. |

### Environment

| Action | Method | Description |
| --- | --- | --- |
| [Get Environment](actions/get-environment.md) | GET | Retrieves an environment from LaunchDarkly. |
| [List Environments](actions/list-environments.md) | GET | Retrieves environments from LaunchDarkly. |
| [Update Environment](actions/update-environment.md) | PUT | Updates an existing environment in LaunchDarkly. |

### Featureflag

| Action | Method | Description |
| --- | --- | --- |
| [Copy Feature Flag](actions/copy-feature-flag.md) | POST | Copies feature flag settings between LaunchDarkly environments. |
| [Create Feature Flag](actions/create-feature-flag.md) | POST | Creates a new feature flag in LaunchDarkly. |
| [Delete Feature Flag](actions/delete-feature-flag.md) | DELETE | Deletes an existing feature flag from LaunchDarkly. |
| [Get Feature Flag](actions/get-feature-flag.md) | GET | Retrieves a feature flag from LaunchDarkly. |
| [List Feature Flags](actions/list-feature-flags.md) | GET | Retrieves feature flags from LaunchDarkly. |
| [Update Feature Flag](actions/update-feature-flag.md) | PUT | Updates an existing feature flag in LaunchDarkly. |

### Flagevaluation

| Action | Method | Description |
| --- | --- | --- |
| [Evaluate Flags](actions/evaluate-flags.md) | GET | Evaluates feature flags for a LaunchDarkly context. |

### Flagstatus

| Action | Method | Description |
| --- | --- | --- |
| [Get Environment Flag Status](actions/get-environment-flag-status.md) | GET | Retrieves a feature flag status for one LaunchDarkly environment. |
| [Get Flag Status](actions/get-flag-status.md) | GET | Retrieves a feature flag status across LaunchDarkly environments. |
| [List Flag Statuses](actions/list-flag-statuses.md) | GET | Retrieves feature flag statuses from LaunchDarkly. |

### Member

| Action | Method | Description |
| --- | --- | --- |
| [List Members](actions/list-members.md) | GET | Retrieves account members from LaunchDarkly. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from LaunchDarkly. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from LaunchDarkly. |

### Segment

| Action | Method | Description |
| --- | --- | --- |
| [Create Segment](actions/create-segment.md) | POST | Creates a new segment in LaunchDarkly. |
| [Delete Segment](actions/delete-segment.md) | DELETE | Deletes an existing segment from LaunchDarkly. |
| [Get Segment](actions/get-segment.md) | GET | Retrieves a segment from LaunchDarkly. |
| [List Segments](actions/list-segments.md) | GET | Retrieves segments from LaunchDarkly. |
| [Update Segment](actions/update-segment.md) | PUT | Updates an existing segment in LaunchDarkly. |

