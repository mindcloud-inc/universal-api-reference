# <img src="https://images.mindcloud.co/apps/icons/hoops_1776695983700.png" alt="Hoops logo" width="28" height="28"> Hoops: Universal API

Manage governed infrastructure access, sessions, and service accounts

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/hoops/latest
- **Category:** IT Operations / Security & Identity
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://hoop.dev
- **Vendor API docs:** https://docs.hoop.dev/beta-docs/api-docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Info](actions/get-user-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hoops/latest/actions/get-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Agent Key

| Action | Method | Description |
| --- | --- | --- |
| [Create Agent Key](actions/create-agent-key.md) | POST |  |
| [Delete Agent Key](actions/delete-agent-key.md) | DELETE |  |
| [List Agent Keys](actions/list-agent-keys.md) | GET |  |

### Connection

| Action | Method | Description |
| --- | --- | --- |
| [Create Connection](actions/create-connection.md) | POST |  |
| [Delete Connection](actions/delete-connection.md) | DELETE |  |
| [Get Connection](actions/get-connection.md) | GET |  |
| [List Connections](actions/list-connections.md) | GET |  |
| [Test Connection](actions/test-connection.md) | GET |  |
| [Update Connection](actions/update-connection.md) | PUT |  |

### Review

| Action | Method | Description |
| --- | --- | --- |
| [Get Review](actions/get-review.md) | GET |  |
| [List Reviews](actions/list-reviews.md) | GET |  |
| [Update Review Status](actions/update-review-status.md) | PUT |  |

### Runbook

| Action | Method | Description |
| --- | --- | --- |
| [List Runbooks](actions/list-runbooks.md) | GET |  |
| [Runbook Exec](actions/runbook-exec.md) | POST |  |

### Search

| Action | Method | Description |
| --- | --- | --- |
| [Search](actions/search.md) | GET |  |

### Service Account

| Action | Method | Description |
| --- | --- | --- |
| [Create Service Account](actions/create-service-account.md) | POST |  |
| [List Service Accounts](actions/list-service-accounts.md) | GET |  |
| [Update Service Account](actions/update-service-account.md) | PUT |  |

### Session

| Action | Method | Description |
| --- | --- | --- |
| [Create Session](actions/create-session.md) | POST |  |
| [Get Session](actions/get-session.md) | GET |  |
| [Kill Session](actions/kill-session.md) | DELETE |  |
| [List Sessions](actions/list-sessions.md) | GET |  |
| [Reviewed Exec](actions/reviewed-exec.md) | PUT |  |
| [Update Session Metadata](actions/update-session-metadata.md) | PUT |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST |  |
| [Delete User](actions/delete-user.md) | DELETE |  |
| [Get User](actions/get-user.md) | GET |  |
| [Get User Info](actions/get-user-info.md) | GET |  |
| [List Users](actions/list-users.md) | GET |  |
| [Update User](actions/update-user.md) | PUT |  |

