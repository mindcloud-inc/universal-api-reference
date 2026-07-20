# Stack AI: Native API Reference

A consolidated summary of Stack AI's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.stackai.com/api-reference/manager
- **API base URL:** `https://api.stack-ai.com`

## Authentication

### Personal API Key

Authenticate with a Stack AI personal API key sent as a Bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.stackai.com/api-reference/manager)

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Custom Tool](actions/create-custom-tool.md) | `POST /tools/custom` | [docs](https://docs.stackai.com/api-reference/tools#post-tools-custom) |
| [Create Folder](actions/create-folder.md) | `PUT /folders` | [docs](https://docs.stackai.com/api-reference/folders#put-folders) |
| [Create Knowledge Base](actions/create-knowledge-base.md) | `POST /v1/knowledge-bases` | [docs](https://docs.stackai.com/api-reference/knowledge-bases#post-v1-knowledge-bases) |
| [Create Resource](actions/create-resource.md) | `POST /v1/knowledge-bases/:knowledge_base_id/resources` | [docs](https://docs.stackai.com/api-reference/knowledge-bases#post-v1-knowledge-bases-knowledge_base_id-resources) |
| [Delete Custom Tool](actions/delete-custom-tool.md) | `DELETE /tools/custom/:provider_id` | [docs](https://docs.stackai.com/api-reference/tools#delete-tools-custom-provider_id) |
| [Delete Folder](actions/delete-folder.md) | `DELETE /folders/:folder_id` | [docs](https://docs.stackai.com/api-reference/folders#delete-folders-folder_id) |
| [Get Action by Provider and ID](actions/get-action-by-provider-and-id.md) | `GET /tools/stackai/providers/:provider_id/actions/:action_id` | [docs](https://docs.stackai.com/api-reference/tools#get-tools-stackai-providers-provider_id-actions-action_id) |
| [Get Action Inputs](actions/get-action-inputs.md) | `GET /tools/stackai/providers/:provider_id/actions/:action_id/inputs` | [docs](https://docs.stackai.com/api-reference/tools#get-tools-stackai-providers-provider_id-actions-action_id-inputs) |
| [Get Action Options](actions/get-action-options.md) | `POST /tools/options` | [docs](https://docs.stackai.com/api-reference/tools#post-tools-options) |
| [Get Action Outputs](actions/get-action-outputs.md) | `GET /tools/stackai/providers/:provider_id/actions/:action_id/outputs` | [docs](https://docs.stackai.com/api-reference/tools#get-tools-stackai-providers-provider_id-actions-action_id-outputs) |
| [Get Folder](actions/get-folder.md) | `GET /folders/:folder_id` | [docs](https://docs.stackai.com/api-reference/folders#get-folders-folder_id) |
| [Get Knowledge Base by ID](actions/get-knowledge-base-by-id.md) | `GET /v1/knowledge-bases/:knowledge_base_id` | [docs](https://docs.stackai.com/api-reference/knowledge-bases#get-v1-knowledge-bases-knowledge_base_id) |
| [Get Resource by ID](actions/get-resource-by-id.md) | `GET /v1/knowledge-bases/:knowledge_base_id/resources/:resource_id` | [docs](https://docs.stackai.com/api-reference/knowledge-bases#get-v1-knowledge-bases-knowledge_base_id-resources-resource_id) |
| [Get StackAI Provider](actions/get-stackai-provider.md) | `GET /tools/stackai/providers/:provider_id` | [docs](https://docs.stackai.com/api-reference/tools#get-tools-stackai-providers-provider_id) |
| [Get Storage Usage](actions/get-storage-usage.md) | `GET /analytics/storage/total-usage` | [docs](https://docs.stackai.com/api-reference/analytics#get-analytics-storage-total-usage) |
| [Get Trigger by Provider and ID](actions/get-trigger-by-provider-and-id.md) | `GET /tools/stackai/providers/:provider_id/triggers/:trigger_id` | [docs](https://docs.stackai.com/api-reference/tools#get-tools-stackai-providers-provider_id-triggers-trigger_id) |
| [Get User Personal Folder](actions/get-user-personal-folder.md) | `GET /folders/me` | [docs](https://docs.stackai.com/api-reference/folders#get-folders-me) |
| [List Custom Tools](actions/list-custom-tools.md) | `GET /tools/custom` | [docs](https://docs.stackai.com/api-reference/tools#get-tools-custom) |
| [List Knowledge Bases](actions/list-knowledge-bases.md) | `GET /v1/knowledge-bases` | [docs](https://docs.stackai.com/api-reference/knowledge-bases#get-v1-knowledge-bases) |
| [List Resources](actions/list-resources.md) | `GET /v1/knowledge-bases/:knowledge_base_id/resources` | [docs](https://docs.stackai.com/api-reference/knowledge-bases#get-v1-knowledge-bases-knowledge_base_id-resources) |
| [List StackAI Actions](actions/list-stackai-actions.md) | `GET /tools/stackai/actions` | [docs](https://docs.stackai.com/api-reference/tools#get-tools-stackai-actions) |
| [List StackAI Providers](actions/list-stackai-providers.md) | `GET /tools/stackai/providers` | [docs](https://docs.stackai.com/api-reference/tools#get-tools-stackai-providers) |
| [List StackAI Tools](actions/list-stackai-tools.md) | `GET /tools/stackai` | [docs](https://docs.stackai.com/api-reference/tools#get-tools-stackai) |
| [List StackAI Triggers](actions/list-stackai-triggers.md) | `GET /tools/stackai/triggers` | [docs](https://docs.stackai.com/api-reference/tools#get-tools-stackai-triggers) |
| [Query Folders](actions/query-folders.md) | `POST /folders` | [docs](https://docs.stackai.com/api-reference/folders#post-folders) |
| [Run Action](actions/run-action.md) | `POST /tools/stackai/providers/:provider_id/actions/:action_id/run` | [docs](https://docs.stackai.com/api-reference/tools#post-tools-stackai-providers-provider_id-actions-action_id-run) |
| [Synchronize Knowledge Base](actions/synchronize-knowledge-base.md) | `POST /v1/knowledge-bases/:knowledge_base_id/sync` | [docs](https://docs.stackai.com/api-reference/knowledge-bases#post-v1-knowledge-bases-knowledge_base_id-sync) |
| [Update Custom Tool](actions/update-custom-tool.md) | `PUT /tools/custom/:provider_id` | [docs](https://docs.stackai.com/api-reference/tools#put-tools-custom-provider_id) |
| [Update Folder](actions/update-folder.md) | `PATCH /folders/:folder_id` | [docs](https://docs.stackai.com/api-reference/folders#patch-folders-folder_id) |
| [Update Knowledge Base](actions/update-knowledge-base.md) | `PATCH /v1/knowledge-bases/:knowledge_base_id` | [docs](https://docs.stackai.com/api-reference/knowledge-bases#patch-v1-knowledge-bases-knowledge_base_id) |
