# <img src="https://images.mindcloud.co/apps/icons/anthropic_1773066096802.png" alt="Anthropic logo" width="28" height="28"> Anthropic: Universal API

Generate text, write code, and build AI agents with Claude.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/anthropic/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.anthropic.com
- **Vendor API docs:** https://platform.claude.com/docs/en/api/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Models](actions/list-models.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/list-models?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Cost Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Cost Report](actions/get-cost-report.md) | GET | Retrieves the current Anthropic cost report. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Delete File](actions/delete-file.md) | DELETE | Deletes an uploaded file from Anthropic. |
| [Download File](actions/download-file.md) | GET | Downloads content for an Anthropic file. |
| [Get File Metadata](actions/get-file-metadata.md) | GET | Retrieves metadata for an Anthropic file. |
| [List Files](actions/list-files.md) | GET | Retrieves uploaded files from the Anthropic account. |
| [Upload File](actions/upload-file.md) | POST | Uploads a new file to Anthropic. |

### Invite

| Action | Method | Description |
| --- | --- | --- |
| [Create Invite](actions/create-invite.md) | POST | Creates an invite for the Anthropic organization. |
| [Delete Invite](actions/delete-invite.md) | DELETE | Deletes an invite from the Anthropic organization. |
| [List Invites](actions/list-invites.md) | GET | Retrieves invites for the Anthropic organization. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Count Message Tokens](actions/count-message-tokens.md) | GET | Counts tokens in an Anthropic message request. |
| [Create Message](actions/create-message.md) | POST | Creates the next message in an Anthropic conversation. |

### Message Batch

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Message Batch](actions/cancel-message-batch.md) | PUT | Cancels a message batch in Anthropic. |
| [Create Message Batch](actions/create-message-batch.md) | POST | Creates a new message batch in Anthropic. |
| [Delete Message Batch](actions/delete-message-batch.md) | DELETE | Deletes a message batch from Anthropic. |
| [List Message Batches](actions/list-message-batches.md) | GET | Retrieves message batches from the Anthropic account. |
| [Retrieve Message Batch](actions/retrieve-message-batch.md) | GET | Retrieves a message batch from Anthropic. |

### Message Batch Result

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Message Batch Results](actions/retrieve-message-batch-results.md) | GET | Retrieves results for an Anthropic message batch. |

### Model

| Action | Method | Description |
| --- | --- | --- |
| [Get Model](actions/get-model.md) | GET | Retrieves a specific model from Anthropic. |
| [List Models](actions/list-models.md) | GET | Retrieves available API models from Anthropic. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Organization](actions/get-current-organization.md) | GET | Retrieves the current Anthropic organization details. |

### Skill

| Action | Method | Description |
| --- | --- | --- |
| [Create Skill](actions/create-skill.md) | POST | Creates a new skill in Anthropic. |
| [Delete Skill](actions/delete-skill.md) | DELETE | Deletes a specific skill from Anthropic. |
| [Get Skill](actions/get-skill.md) | GET | Retrieves a specific skill from Anthropic. |
| [List Skills](actions/list-skills.md) | GET | Retrieves skills from the Anthropic account. |

### Skill Version

| Action | Method | Description |
| --- | --- | --- |
| [List Skill Versions](actions/list-skill-versions.md) | GET | Retrieves versions for an Anthropic skill. |

### Usage Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Messages Usage Report](actions/get-messages-usage-report.md) | GET | Retrieves the Anthropic messages usage report. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves users in the Anthropic organization. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Create Workspace](actions/create-workspace.md) | POST | Creates a workspace in the Anthropic organization. |
| [List Workspaces](actions/list-workspaces.md) | GET | Retrieves workspaces in the Anthropic organization. |

### Workspace Member

| Action | Method | Description |
| --- | --- | --- |
| [Create Workspace Member](actions/create-workspace-member.md) | POST | Adds a member to an Anthropic workspace. |

