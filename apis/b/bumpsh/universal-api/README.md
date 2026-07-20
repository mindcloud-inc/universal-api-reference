# <img src="https://images.mindcloud.co/apps/icons/bumpsh_1776343053197.png" alt="Bump.sh logo" width="28" height="28"> Bump.sh: Universal API

Create, preview, validate, and manage API documentation

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bumpsh/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://bump.sh
- **Vendor API docs:** https://developers.bump.sh/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Hubs](actions/list-hubs.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bumpsh/latest/actions/list-hubs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Branch

| Action | Method | Description |
| --- | --- | --- |
| [Create Branch](actions/create-branch.md) | POST | Creates a new branch in Bump.sh. |
| [Delete Branch](actions/delete-branch.md) | DELETE | Deletes an existing branch from Bump.sh. |
| [List Branches](actions/list-branches.md) | GET | Retrieves branches from a Bump.sh documentation. |
| [Set Default Branch](actions/set-default-branch.md) | PUT | Sets the default branch for a Bump.sh documentation. |

### Diff

| Action | Method | Description |
| --- | --- | --- |
| [Create Diff](actions/create-diff.md) | POST | Creates a diff in Bump.sh. |
| [Get Diff](actions/get-diff.md) | GET | Retrieves a diff from Bump.sh. |

### Hub

| Action | Method | Description |
| --- | --- | --- |
| [Get Hub](actions/get-hub.md) | GET | Retrieves a hub from Bump.sh. |
| [List Hubs](actions/list-hubs.md) | GET | Retrieves hubs from Bump.sh. |

### Mcpserverdocument

| Action | Method | Description |
| --- | --- | --- |
| [Deploy MCP Server Document](actions/deploy-mcp-server-document.md) | POST |  |

### Preview

| Action | Method | Description |
| --- | --- | --- |
| [Create Preview](actions/create-preview.md) | POST | Creates a preview in Bump.sh. |
| [Update Preview](actions/update-preview.md) | PUT | Updates an existing preview in Bump.sh. |

### Statuscheck

| Action | Method | Description |
| --- | --- | --- |
| [Ping](actions/ping.md) | GET | Checks the Bump.sh API status. |

### Validation

| Action | Method | Description |
| --- | --- | --- |
| [Validate Definition](actions/validate-definition.md) | POST | Validates a documentation definition in Bump.sh. |

### Version

| Action | Method | Description |
| --- | --- | --- |
| [Create Version](actions/create-version.md) | POST | Creates a new documentation version in Bump.sh. |
| [Get Version](actions/get-version.md) | GET | Retrieves a documentation version from Bump.sh. |

