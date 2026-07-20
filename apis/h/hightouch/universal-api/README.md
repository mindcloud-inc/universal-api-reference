# <img src="https://images.mindcloud.co/apps/icons/hightouch_1776886606866.png" alt="Hightouch logo" width="28" height="28"> Hightouch: Universal API

Manage Hightouch sources, models, syncs, and event contracts

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/hightouch/latest
- **Category:** Marketing
- **Actions:** 36
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://hightouch.com
- **Vendor API docs:** https://hightouch.com/docs/developer-tools/api-guide

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Destinations](actions/list-destinations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/list-destinations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (36)

### Decision Engine Flow

| Action | Method | Description |
| --- | --- | --- |
| [Get Decision Engine Flow](actions/get-decision-engine-flow.md) | GET | Retrieves a decision engine flow from Hightouch. |
| [List Decision Engine Flows](actions/list-decision-engine-flows.md) | GET | Retrieves decision engine flows from Hightouch. |

### Decision Engine Flow Run

| Action | Method | Description |
| --- | --- | --- |
| [Trigger Decision Engine Flow Run](actions/trigger-decision-engine-flow-run.md) | POST | Triggers a decision engine flow run in Hightouch. |

### Decision Engine Message

| Action | Method | Description |
| --- | --- | --- |
| [Create Decision Engine Message](actions/create-decision-engine-message.md) | POST | Creates a decision engine message in Hightouch. |
| [Get Decision Engine Message](actions/get-decision-engine-message.md) | GET | Retrieves a decision engine message from Hightouch. |
| [List Decision Engine Messages](actions/list-decision-engine-messages.md) | GET | Retrieves decision engine messages from Hightouch. |
| [Update Decision Engine Message](actions/update-decision-engine-message.md) | PUT | Updates a decision engine message in Hightouch. |

### Destination

| Action | Method | Description |
| --- | --- | --- |
| [Create Destination](actions/create-destination.md) | POST | Creates a new destination in Hightouch. |
| [Get Destination](actions/get-destination.md) | GET | Retrieves a destination from Hightouch. |
| [List Destinations](actions/list-destinations.md) | GET | Retrieves destinations from Hightouch. |
| [Update Destination](actions/update-destination.md) | PUT | Updates an existing destination in Hightouch. |

### Event Contract

| Action | Method | Description |
| --- | --- | --- |
| [Create Event Contract](actions/create-event-contract.md) | POST | Creates a new event contract in Hightouch. |
| [Get Event Contract](actions/get-event-contract.md) | GET | Retrieves an event contract from Hightouch. |
| [List Event Contracts](actions/list-event-contracts.md) | GET | Retrieves event contracts from Hightouch. |
| [Update Event Contract](actions/update-event-contract.md) | PUT | Updates an event contract in Hightouch. |

### Idr Reprocessing Request

| Action | Method | Description |
| --- | --- | --- |
| [Get IDR Reprocess Status](actions/get-idr-reprocess-status.md) | GET | Retrieves IDR reprocessing status from Hightouch. |
| [Queue IDR Identifiers For Reprocessing](actions/queue-idr-identifiers-for-reprocessing.md) | POST | Queues IDR identifiers for reprocessing in Hightouch. |

### Idr Run

| Action | Method | Description |
| --- | --- | --- |
| [List IDR Runs](actions/list-idr-runs.md) | GET | Retrieves IDR runs from Hightouch. |
| [Trigger IDR Run](actions/trigger-idr-run.md) | POST | Triggers an IDR run in Hightouch. |

### Model

| Action | Method | Description |
| --- | --- | --- |
| [Create Model](actions/create-model.md) | POST | Creates a new model in Hightouch. |
| [Get Model](actions/get-model.md) | GET | Retrieves a model from Hightouch. |
| [List Models](actions/list-models.md) | GET | Retrieves models from Hightouch. |
| [Update Model](actions/update-model.md) | PUT | Updates an existing model in Hightouch. |

### Source

| Action | Method | Description |
| --- | --- | --- |
| [Create Source](actions/create-source.md) | POST | Creates a new source in Hightouch. |
| [Get Source](actions/get-source.md) | GET | Retrieves a source from Hightouch. |
| [List Sources](actions/list-sources.md) | GET | Retrieves sources from Hightouch. |
| [Update Source](actions/update-source.md) | PUT | Updates an existing source in Hightouch. |

### Sync

| Action | Method | Description |
| --- | --- | --- |
| [Create Sync](actions/create-sync.md) | POST | Creates a new sync in Hightouch. |
| [Get Sync](actions/get-sync.md) | GET | Retrieves a sync from Hightouch. |
| [List Syncs](actions/list-syncs.md) | GET | Retrieves syncs from Hightouch. |
| [Update Sync](actions/update-sync.md) | PUT | Updates an existing sync in Hightouch. |

### Sync Run

| Action | Method | Description |
| --- | --- | --- |
| [List Sync Runs](actions/list-sync-runs.md) | GET | Retrieves sync runs from Hightouch. |
| [Trigger Sync](actions/trigger-sync.md) | POST | Triggers a sync run in Hightouch. |
| [Trigger Sync From ID or Slug](actions/trigger-sync-from-id-or-slug.md) | POST | Triggers a sync run in Hightouch by ID or slug. |

### Sync Sequence Run

| Action | Method | Description |
| --- | --- | --- |
| [Get Sync Sequence Run](actions/get-sync-sequence-run.md) | GET | Retrieves a sync sequence run from Hightouch. |
| [Trigger Sync Sequence](actions/trigger-sync-sequence.md) | POST | Triggers a sync sequence in Hightouch. |

