# <img src="https://images.mindcloud.co/apps/icons/apify_1773335051928.png" alt="Apify logo" width="28" height="28"> Apify: Universal API

Connect Apify to list and manage actors, tasks, runs, datasets, key-value stores, request queues, webhooks, schedules, logs, and account data through the Apify API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/apify/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://apify.com
- **Vendor API docs:** https://docs.apify.com/api/v2

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Private User Data](actions/get-private-user-data.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apify/latest/actions/get-private-user-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Account Limit

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Limits](actions/get-account-limits.md) | GET | Retrieves account limits from Apify. |

### Actor

| Action | Method | Description |
| --- | --- | --- |
| [Get Actor](actions/get-actor.md) | GET | Retrieves an actor from Apify. |
| [List Actors](actions/list-actors.md) | GET | Retrieves actors from Apify. |

### Actor Build

| Action | Method | Description |
| --- | --- | --- |
| [Get Actor Build](actions/get-actor-build.md) | GET | Retrieves an actor build from Apify. |
| [List Actor Builds](actions/list-actor-builds.md) | GET | Retrieves actor builds for an Apify actor. |

### Actor Run

| Action | Method | Description |
| --- | --- | --- |
| [Get Actor Run](actions/get-actor-run.md) | GET | Retrieves an actor run from Apify. |
| [Get Last Actor Run](actions/get-last-actor-run.md) | GET | Retrieves the last run for an Apify actor. |
| [List Actor Runs](actions/list-actor-runs.md) | GET | Retrieves actor runs for an Apify actor. |

### Actor Task

| Action | Method | Description |
| --- | --- | --- |
| [Get Actor Task](actions/get-actor-task.md) | GET | Retrieves an actor task from Apify. |
| [List Actor Tasks](actions/list-actor-tasks.md) | GET | Retrieves actor tasks from Apify. |

### Actor Task Input

| Action | Method | Description |
| --- | --- | --- |
| [Get Actor Task Input](actions/get-actor-task-input.md) | GET | Retrieves input for an Apify actor task. |

### Actor Version

| Action | Method | Description |
| --- | --- | --- |
| [List Actor Versions](actions/list-actor-versions.md) | GET | Retrieves actor versions for an Apify actor. |

### Dataset

| Action | Method | Description |
| --- | --- | --- |
| [Get Dataset](actions/get-dataset.md) | GET | Retrieves a dataset from Apify. |
| [List Datasets](actions/list-datasets.md) | GET | Retrieves datasets from Apify. |

### Dataset Item

| Action | Method | Description |
| --- | --- | --- |
| [Get Dataset Items](actions/get-dataset-items.md) | GET | Retrieves items from an Apify dataset. |

### Dataset Statistics

| Action | Method | Description |
| --- | --- | --- |
| [Get Dataset Statistics](actions/get-dataset-statistics.md) | GET | Retrieves statistics for an Apify dataset. |

### Key-value Store

| Action | Method | Description |
| --- | --- | --- |
| [Get Key-Value Store](actions/get-key-value-store.md) | GET | Retrieves a key-value store from Apify. |
| [List Key-Value Stores](actions/list-key-value-stores.md) | GET | Retrieves key-value stores from Apify. |

### Monthly Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Monthly Usage](actions/get-monthly-usage.md) | GET | Retrieves monthly usage from Apify. |

### Request Queue

| Action | Method | Description |
| --- | --- | --- |
| [Get Request Queue](actions/get-request-queue.md) | GET | Retrieves a request queue from Apify. |
| [List Request Queues](actions/list-request-queues.md) | GET | Retrieves request queues from Apify. |

### Task Run

| Action | Method | Description |
| --- | --- | --- |
| [Get Last Actor Task Run](actions/get-last-actor-task-run.md) | GET | Retrieves the last run for an Apify actor task. |
| [List Actor Task Runs](actions/list-actor-task-runs.md) | GET | Retrieves runs for an Apify actor task. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Private User Data](actions/get-private-user-data.md) | GET | Retrieves private user data from Apify. |

