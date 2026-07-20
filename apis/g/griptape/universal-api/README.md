# <img src="https://images.mindcloud.co/apps/icons/griptape_1774968397408.png" alt="Griptape logo" width="28" height="28"> Griptape: Universal API

Operate Griptape Cloud resources including threads, rulesets, assistants, structures, tools, knowledge bases, data sources, and bucket assets.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/griptape/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.griptape.ai/
- **Vendor API docs:** https://docs.griptape.ai/stable/griptape-cloud/api/api-reference/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Threads](actions/list-threads.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/griptape/latest/actions/list-threads?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Activities

| Action | Method | Description |
| --- | --- | --- |
| [Run Tool Activity](actions/run-tool-activity.md) | POST | Runs a tool activity in Griptape. |

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [Get Bucket Asset URL](actions/get-bucket-asset-url.md) | GET | Retrieves a signed bucket asset URL from Griptape. |
| [List Bucket Assets](actions/list-bucket-assets.md) | GET | Finds assets in a Griptape bucket. |
| [Save Bucket Asset](actions/save-bucket-asset.md) | PUT | Creates a bucket asset record in Griptape. |

### Assistant

| Action | Method | Description |
| --- | --- | --- |
| [Run Assistant](actions/run-assistant.md) | POST | Runs an assistant in Griptape. |

### Bucket

| Action | Method | Description |
| --- | --- | --- |
| [Get Bucket](actions/get-bucket.md) | GET | Retrieves a bucket from Griptape. |
| [List Buckets](actions/list-buckets.md) | GET | Finds buckets in Griptape. |

### Data

| Action | Method | Description |
| --- | --- | --- |
| [List Data Sources](actions/list-data-sources.md) | GET | Finds data sources in Griptape. |
| [Refresh Data Source](actions/refresh-data-source.md) | POST | Creates a data source refresh job in Griptape. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Send Structure Run Event](actions/send-structure-run-event.md) | POST | Sends a structure run event to Griptape. |
| [Stream Assistant Run Events](actions/stream-assistant-run-events.md) | GET | Streams assistant run events from Griptape. |

### Knowledge

| Action | Method | Description |
| --- | --- | --- |
| [List Knowledge Bases](actions/list-knowledge-bases.md) | GET | Finds knowledge bases in Griptape. |
| [Query Knowledge Base](actions/query-knowledge-base.md) | GET | Queries a knowledge base in Griptape. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [List Thread Messages](actions/list-thread-messages.md) | GET | Finds messages in a Griptape thread. |

### Rule

| Action | Method | Description |
| --- | --- | --- |
| [List Rules In Ruleset](actions/list-rules-in-ruleset.md) | GET | Finds rules in a Griptape ruleset. |

### Ruleset

| Action | Method | Description |
| --- | --- | --- |
| [Get Ruleset](actions/get-ruleset.md) | GET | Retrieves a ruleset from Griptape. |
| [List Rulesets](actions/list-rulesets.md) | GET | Finds rulesets in Griptape. |

### Structure

| Action | Method | Description |
| --- | --- | --- |
| [List Structures](actions/list-structures.md) | GET | Finds structures in Griptape. |
| [Run Structure](actions/run-structure.md) | POST | Runs a structure in Griptape. |

### Threads

| Action | Method | Description |
| --- | --- | --- |
| [Create Thread](actions/create-thread.md) | POST | Creates a new thread in Griptape. |
| [Get Thread](actions/get-thread.md) | GET | Retrieves a thread from Griptape. |
| [List Threads](actions/list-threads.md) | GET | Finds threads in Griptape. |
| [Update Thread](actions/update-thread.md) | PUT | Updates an existing thread in Griptape. |

### Tool

| Action | Method | Description |
| --- | --- | --- |
| [Get Tool OpenAPI](actions/get-tool-open-api.md) | GET | Retrieves a tool OpenAPI schema from Griptape. |
| [List Tools](actions/list-tools.md) | GET | Finds tools in Griptape. |

