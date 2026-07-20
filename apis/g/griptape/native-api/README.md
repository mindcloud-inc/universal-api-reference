# Griptape: Native API Reference

A consolidated summary of Griptape's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://docs.griptape.ai/stable/griptape-cloud/api/api-reference/
- **API base URL:** `https://cloud.griptape.ai`

## Authentication

### API Key

Authenticate with a Griptape Cloud API key using the standard bearer token header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.griptape.ai/stable/griptape-cloud/structures/run-structure/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Thread](actions/create-thread.md) | `POST /api/threads` | [docs](https://docs.griptape.ai/stable/griptape-cloud/threads/threads/) |
| [Get Bucket](actions/get-bucket.md) | `GET /api/buckets/:bucket_id` | [docs](https://docs.griptape.ai/stable/griptape-cloud/data-lakes/data-lakes/) |
| [Get Bucket Asset URL](actions/get-bucket-asset-url.md) | `POST /api/buckets/:bucket_id/asset-urls/:full_key` | [docs](https://docs.griptape.ai/stable/griptape-cloud/data-lakes/data-lakes/) |
| [Get Ruleset](actions/get-ruleset.md) | `GET /api/rulesets/:ruleset_id` | [docs](https://docs.griptape.ai/stable/griptape-cloud/rules/rulesets/) |
| [Get Thread](actions/get-thread.md) | `GET /api/threads/:thread_id` | [docs](https://docs.griptape.ai/stable/griptape-cloud/threads/threads/) |
| [Get Tool OpenAPI](actions/get-tool-open-api.md) | `GET /api/tools/:tool_id/openapi` | [docs](https://docs.griptape.ai/stable/griptape-cloud/tools/run-tool/) |
| [List Bucket Assets](actions/list-bucket-assets.md) | `GET /api/buckets/:bucket_id/assets` | [docs](https://docs.griptape.ai/stable/griptape-cloud/data-lakes/data-lakes/) |
| [List Buckets](actions/list-buckets.md) | `GET /api/buckets` | [docs](https://docs.griptape.ai/stable/griptape-cloud/data-lakes/data-lakes/) |
| [List Data Sources](actions/list-data-sources.md) | `GET /api/data-connectors` | [docs](https://docs.griptape.ai/stable/griptape-cloud/data-sources/what-are-data-sources/) |
| [List Knowledge Bases](actions/list-knowledge-bases.md) | `GET /api/knowledge-bases` | [docs](https://docs.griptape.ai/stable/griptape-cloud/knowledge-bases/what-are-knowledge-bases/) |
| [List Rules In Ruleset](actions/list-rules-in-ruleset.md) | `GET /api/rules` | [docs](https://docs.griptape.ai/stable/griptape-cloud/rules/rulesets/) |
| [List Rulesets](actions/list-rulesets.md) | `GET /api/rulesets` | [docs](https://docs.griptape.ai/stable/griptape-cloud/rules/rulesets/) |
| [List Structures](actions/list-structures.md) | `GET /api/structures` | [docs](https://docs.griptape.ai/stable/griptape-cloud/structures/what-are-structures/) |
| [List Thread Messages](actions/list-thread-messages.md) | `GET /api/threads/:thread_id/messages` | [docs](https://docs.griptape.ai/stable/griptape-cloud/threads/threads/) |
| [List Threads](actions/list-threads.md) | `GET /api/threads` | [docs](https://docs.griptape.ai/stable/griptape-cloud/threads/threads/) |
| [List Tools](actions/list-tools.md) | `GET /api/tools` | [docs](https://docs.griptape.ai/stable/griptape-cloud/tools/create-tool/) |
| [Query Knowledge Base](actions/query-knowledge-base.md) | `POST /api/knowledge-bases/:knowledge_base_id/query` | [docs](https://docs.griptape.ai/stable/griptape-cloud/knowledge-bases/accessing-data/) |
| [Refresh Data Source](actions/refresh-data-source.md) | `POST /api/data-connectors/:data_source_id/data-jobs` | [docs](https://docs.griptape.ai/stable/griptape-cloud/data-sources/refresh-data/) |
| [Run Assistant](actions/run-assistant.md) | `POST /api/assistants/:assistant_id/runs` | [docs](https://docs.griptape.ai/stable/griptape-cloud/assistants/assistant-runs/) |
| [Run Structure](actions/run-structure.md) | `POST /api/structures/:structure_id/runs` | [docs](https://docs.griptape.ai/stable/griptape-cloud/structures/run-structure/) |
| [Run Tool Activity](actions/run-tool-activity.md) | `POST /api/tools/:tool_id/activities/:activity_name` | [docs](https://docs.griptape.ai/stable/griptape-cloud/tools/run-tool/) |
| [Save Bucket Asset](actions/save-bucket-asset.md) | `PUT /api/buckets/:bucket_id/assets` | [docs](https://docs.griptape.ai/stable/griptape-cloud/data-lakes/data-lakes/) |
| [Send Structure Run Event](actions/send-structure-run-event.md) | `POST /api/structure-runs/:structure_run_id/events` | [docs](https://docs.griptape.ai/stable/griptape-cloud/structures/structure-run-events/) |
| [Stream Assistant Run Events](actions/stream-assistant-run-events.md) | `GET /api/assistant-runs/:assistant_run_id/events/stream` | [docs](https://docs.griptape.ai/stable/griptape-cloud/assistants/assistant-runs/) |
| [Update Thread](actions/update-thread.md) | `PATCH /api/threads/:thread_id` | [docs](https://docs.griptape.ai/stable/griptape-cloud/threads/threads/) |
