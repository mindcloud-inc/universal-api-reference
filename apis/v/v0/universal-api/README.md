# <img src="https://images.mindcloud.co/apps/icons/v0_1774285054956.png" alt="v0 logo" width="28" height="28"> v0: Universal API

Build, manage, and deploy AI-generated web apps with v0

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/v0/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://v0.dev
- **Vendor API docs:** https://v0.app/docs/api/platform/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User](actions/get-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/v0/latest/actions/get-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Billing

| Action | Method | Description |
| --- | --- | --- |
| [Get Billing](actions/get-billing.md) | GET | Retrieves billing details for the current user in v0. |

### Chat

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat](actions/create-chat.md) | POST | Creates a new chat in v0. |
| [Find Chats](actions/find-chats.md) | GET | Finds chats in the v0 workspace. |
| [Get Chat](actions/get-chat.md) | GET | Retrieves a chat from v0 by ID. |
| [Initialize Chat](actions/initialize-chat.md) | POST | Initializes a new chat in v0 from source content. |
| [Update Chat](actions/update-chat.md) | PUT | Updates an existing chat in v0. |

### Deployment

| Action | Method | Description |
| --- | --- | --- |
| [Create Deployment](actions/create-deployment.md) | POST | Creates a new deployment in v0. |
| [Find Deployments](actions/find-deployments.md) | GET | Finds deployments in the v0 workspace. |

### Deployment Log

| Action | Method | Description |
| --- | --- | --- |
| [Find Deployment Logs](actions/find-deployment-logs.md) | GET | Finds logs for a v0 deployment. |

### Environment Variable

| Action | Method | Description |
| --- | --- | --- |
| [Create Environment Variables](actions/create-environment-variables.md) | POST | Creates project environment variables in v0. |
| [Find Environment Variables](actions/find-environment-variables.md) | GET | Finds project environment variables in v0. |
| [Update Environment Variables](actions/update-environment-variables.md) | PUT | Updates project environment variables in v0. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Find Chat Messages](actions/find-chat-messages.md) | GET | Finds messages in a v0 chat. |
| [Send Message](actions/send-message.md) | POST | Sends a message to an existing v0 chat. |

### Plan

| Action | Method | Description |
| --- | --- | --- |
| [Get Plan](actions/get-plan.md) | GET | Retrieves the current plan from v0. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in v0. |
| [Find Projects](actions/find-projects.md) | GET | Finds projects in the v0 workspace. |
| [Get Project by ID](actions/get-project-by-id.md) | GET | Retrieves a project from v0 by ID. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in v0. |

### Rate Limit

| Action | Method | Description |
| --- | --- | --- |
| [Find Rate Limit](actions/find-rate-limit.md) | GET | Retrieves rate limit details from v0. |

### Scope

| Action | Method | Description |
| --- | --- | --- |
| [Get User Scopes](actions/get-user-scopes.md) | GET | Retrieves the current user scopes from v0. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves the current user from v0. |

### Version

| Action | Method | Description |
| --- | --- | --- |
| [Find Chat Versions](actions/find-chat-versions.md) | GET | Finds versions for a v0 chat. |
| [Get Chat Version](actions/get-chat-version.md) | GET | Retrieves a chat version from v0 by ID. |

