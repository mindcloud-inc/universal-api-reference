# <img src="https://images.mindcloud.co/apps/icons/apple-touch-icon-1_1775061402155.png" alt="Faraday logo" width="28" height="28"> Faraday: Universal API

Faraday's API helps teams predict customer behavior programmatically and manage accounts, traits, streams, usage, and webhook endpoints.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/faraday/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 32
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://faraday.ai
- **Vendor API docs:** https://faraday.ai/docs/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current Account Usage](actions/get-current-account-usage.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/faraday/latest/actions/get-current-account-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (32)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Create Account](actions/create-account.md) | POST | Creates a new subaccount in Faraday. |
| [Delete Account](actions/delete-account.md) | DELETE | Requests deletion of an existing account from Faraday. |
| [List Accounts](actions/list-accounts.md) | GET | Retrieves a list of accounts from Faraday. |
| [Retrieve Account](actions/retrieve-account.md) | GET | Retrieves a specific account from Faraday. |
| [Retrieve Current Account](actions/retrieve-current-account.md) | GET | Retrieves the current account from Faraday. |
| [Update Account](actions/update-account.md) | PUT | Updates an existing account in Faraday. |

### Billing

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Account Billing](actions/get-current-account-billing.md) | GET | Retrieves current account billing details from Faraday. |

### Stream

| Action | Method | Description |
| --- | --- | --- |
| [Archive Stream](actions/archive-stream.md) | PUT | Archives an existing stream in Faraday. |
| [Create Stream](actions/create-stream.md) | POST | Finds a stream in Faraday, or creates one if needed. |
| [Delete Stream](actions/delete-stream.md) | DELETE | Deletes an existing stream from Faraday. |
| [Force Update Stream](actions/force-update-stream.md) | PUT | Triggers a rerun for a stream in Faraday. |
| [Get Stream](actions/get-stream.md) | GET | Retrieves a stream from Faraday. |
| [List Streams](actions/list-streams.md) | GET | Retrieves a list of streams from Faraday. |
| [Unarchive Stream](actions/unarchive-stream.md) | PUT | Unarchives an existing stream in Faraday. |

### Stream Analysis

| Action | Method | Description |
| --- | --- | --- |
| [Get Stream Analysis](actions/get-stream-analysis.md) | GET | Retrieves stream event counts from Faraday. |

### Trait

| Action | Method | Description |
| --- | --- | --- |
| [Archive Trait](actions/archive-trait.md) | PUT | Archives an existing trait in Faraday. |
| [Create Trait](actions/create-trait.md) | POST | Creates a new user-defined trait in Faraday. |
| [Delete Trait](actions/delete-trait.md) | DELETE | Deletes an existing trait from Faraday. |
| [Force Update Trait](actions/force-update-trait.md) | PUT | Triggers a rerun for a trait in Faraday. |
| [Get Trait](actions/get-trait.md) | GET | Retrieves a trait from Faraday. |
| [List Traits](actions/list-traits.md) | GET | Retrieves a list of traits from Faraday. |
| [Unarchive Trait](actions/unarchive-trait.md) | PUT | Unarchives an existing trait in Faraday. |
| [Update Trait](actions/update-trait.md) | PUT | Updates an existing trait in Faraday. |

### Trait Analysis

| Action | Method | Description |
| --- | --- | --- |
| [Get Trait Analysis Dimensions](actions/get-trait-analysis-dimensions.md) | GET | Retrieves trait analysis dimensions from Faraday. |

### Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Usage](actions/get-account-usage.md) | GET | Retrieves account usage metrics from Faraday. |
| [Get Current Account Usage](actions/get-current-account-usage.md) | GET | Retrieves current account usage metrics from Faraday. |
| [Get Usage Stats](actions/get-usage-stats.md) | GET | Retrieves account usage stats from Faraday. |

### Webhook Endpoint

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook Endpoint](actions/create-webhook-endpoint.md) | POST | Creates a new webhook endpoint in Faraday. |
| [Delete Webhook Endpoint](actions/delete-webhook-endpoint.md) | DELETE | Deletes an existing webhook endpoint from Faraday. |
| [List Webhook Endpoints](actions/list-webhook-endpoints.md) | GET | Retrieves a list of webhook endpoints from Faraday. |
| [Retrieve Webhook Endpoint](actions/retrieve-webhook-endpoint.md) | GET | Retrieves a webhook endpoint from Faraday. |
| [Update Webhook Endpoint](actions/update-webhook-endpoint.md) | PUT | Updates an existing webhook endpoint in Faraday. |

