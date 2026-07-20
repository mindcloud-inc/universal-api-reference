# <img src="https://images.mindcloud.co/apps/icons/middesk-icon-96_1776353536433.png" alt="Middesk logo" width="28" height="28"> Middesk: Universal API

Middesk provides business verification, entity management, onboarding, monitoring, agents, webhooks, documents, and related KYB workflows through its REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/middesk/latest
- **Category:** IT Operations / Security & Identity
- **Actions:** 68
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.middesk.com
- **Vendor API docs:** https://docs.middesk.com/build/api-keys

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get TIN Match Availability](actions/get-tin-match-availability.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/middesk/latest/actions/get-tin-match-availability?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (68)

### Action

| Action | Method | Description |
| --- | --- | --- |
| [Create an action on an object](actions/create-action.md) | POST | Creates an action on an object in Middesk. |
| [Retrieve an action](actions/get-action.md) | GET | Retrieves an action from your Middesk account. |
| [List actions for an object](actions/list-actions.md) | GET | Retrieves actions for an object from Middesk. |

### Agent

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve an agent](actions/get-agent.md) | GET | Retrieves an agent from your Middesk account. |
| [List agents](actions/list-agents.md) | GET | Retrieves agents from your Middesk account. |

### Agent Run

| Action | Method | Description |
| --- | --- | --- |
| [Create an agent run](actions/create-agent-run.md) | POST | Creates an agent run in Middesk. |
| [Retrieve an agent run](actions/get-agent-run.md) | GET | Retrieves an agent run from Middesk. |
| [List agent runs](actions/list-agent-runs.md) | GET | Retrieves agent runs from your Middesk account. |

### Agent Run Event Stream

| Action | Method | Description |
| --- | --- | --- |
| [Stream agent run events](actions/stream-agent-run-events.md) | GET | Retrieves streamed events for a Middesk agent run. |

### Agent Thread

| Action | Method | Description |
| --- | --- | --- |
| [Create an agent thread](actions/create-agent-thread.md) | POST | Creates an agent thread in Middesk. |
| [Retrieve an agent thread](actions/get-agent-thread.md) | GET | Retrieves an agent thread from Middesk. |
| [List agent threads](actions/list-agent-threads.md) | GET | Retrieves agent threads from your Middesk account. |

### Application

| Action | Method | Description |
| --- | --- | --- |
| [Create an application](actions/create-application.md) | POST | Creates an application in your Middesk account. |

### Business

| Action | Method | Description |
| --- | --- | --- |
| [Create a business](actions/create-business.md) | POST | Creates a business in your Middesk account. |
| [Retrieve a business](actions/get-business.md) | GET | Retrieves a business from your Middesk account. |
| [List Businesses](actions/list-businesses.md) | GET | Retrieves businesses from your Middesk account. |
| [Update a business](actions/update-business.md) | PUT | Updates a business in your Middesk account. |

### Business Batch

| Action | Method | Description |
| --- | --- | --- |
| [Create a business batch](actions/create-business-batch.md) | POST | Creates a business batch in Middesk. |
| [Retrieve a business batch](actions/get-business-batch.md) | GET | Retrieves a business batch from Middesk. |
| [List business batches](actions/list-business-batches.md) | GET | Retrieves business batches from your Middesk account. |

### Business Batch Csv

| Action | Method | Description |
| --- | --- | --- |
| [Download business batch CSV](actions/get-business-batch-csv.md) | GET | Retrieves a business batch CSV from Middesk. |

### Business Document

| Action | Method | Description |
| --- | --- | --- |
| [List documents for a business](actions/list-documents.md) | GET | Retrieves business documents from your Middesk account. |

### Business Identity Suggestion

| Action | Method | Description |
| --- | --- | --- |
| [Autocomplete business identities](actions/autocomplete-business-identities.md) | POST | Autocompletes business identities in your Middesk account. |

### Business Lien

| Action | Method | Description |
| --- | --- | --- |
| [Create a lien for a business](actions/create-lien.md) | POST | Creates a lien for a business in Middesk. |
| [List liens for a business](actions/list-liens.md) | GET | Retrieves liens for a business in Middesk. |

### Business Lien Filing Batch

| Action | Method | Description |
| --- | --- | --- |
| [Create lien filings in batch](actions/create-lien-filings-in-batch.md) | POST | Creates lien filings in batch in Middesk. |

### Business Monitor

| Action | Method | Description |
| --- | --- | --- |
| [Create a monitor for a business](actions/create-business-monitor.md) | POST | Creates a business monitor in Middesk. |
| [Delete a monitor for a business](actions/delete-business-monitor.md) | DELETE | Deletes a business monitor from Middesk. |
| [Retrieve a monitor for a business](actions/get-business-monitor.md) | GET | Retrieves a business monitor from Middesk. |
| [Update a monitor for a business](actions/update-business-monitor.md) | PUT | Updates a business monitor in Middesk. |

### Business Order

| Action | Method | Description |
| --- | --- | --- |
| [Create an order for a business](actions/create-order.md) | POST | Creates an order for a business in Middesk. |
| [Retrieve an order](actions/get-order.md) | GET | Retrieves an order from your Middesk account. |

### Business Orders

| Action | Method | Description |
| --- | --- | --- |
| [List orders for a business](actions/list-orders.md) | GET | Retrieves orders for a business in Middesk. |

### Business Pdf

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve a business PDF](actions/get-business-pdf.md) | GET | Retrieves a business PDF from Middesk. |

### Business Policy Result

| Action | Method | Description |
| --- | --- | --- |
| [List policy results for a business](actions/list-business-policy-results.md) | GET | Retrieves policy results for a business in Middesk. |

### Business Prefill

| Action | Method | Description |
| --- | --- | --- |
| [Prefill business information](actions/business.md) | POST | Prefills business information in your Middesk account. |

### Business Review

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve a review for a business](actions/get-business-review.md) | GET | Retrieves a business review from Middesk. |

### Business Timeline

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve timeline for a business](actions/get-business-timeline.md) | GET | Retrieves a business timeline from Middesk. |

### Business Website Analysis

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve website analysis for a business](actions/get-business-website.md) | GET | Retrieves website analysis for a business in Middesk. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Create a company](actions/create-company.md) | POST | Creates a company in your Middesk account. |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Get a document](actions/get-document.md) | GET | Retrieves a document from your Middesk account. |

### Document Download Url

| Action | Method | Description |
| --- | --- | --- |
| [Get document download URL](actions/get-document-download-url.md) | GET | Retrieves a document download URL from Middesk. |

### Information Request

| Action | Method | Description |
| --- | --- | --- |
| [List Information Requests](actions/list-information-requests.md) | GET | Retrieves information requests from your Middesk account. |

### Jurisdiction

| Action | Method | Description |
| --- | --- | --- |
| [Fetch supported local jurisdictions](actions/list-jurisdictions.md) | GET | Retrieves supported local jurisdictions from Middesk. |

### Lien Termination

| Action | Method | Description |
| --- | --- | --- |
| [Create a termination for a lien](actions/create-lien-termination.md) | POST | Creates a lien termination in Middesk. |

### Mail Item

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve a mail item](actions/get-mail-item.md) | GET | Retrieves a mail item from Middesk. |
| [List mail items](actions/list-mail-items.md) | GET | Retrieves mail items from your Middesk account. |
| [Update a mail item](actions/update-mail-item.md) | PUT | Updates a mail item in Middesk. |

### Monitor Bulk Disable

| Action | Method | Description |
| --- | --- | --- |
| [Bulk disable monitors](actions/bulk-disable-monitors.md) | POST | Disables business monitors in bulk in Middesk. |

### Oidc Public Key

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve OIDC public keys](actions/get-oidc-keys.md) | GET | Retrieves OIDC public keys from Middesk. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve an order by ID](actions/get-order-by-id.md) | GET | Retrieves an order from Middesk by ID. |
| [Update an order](actions/update-order.md) | PUT | Updates an order in your Middesk account. |

### Question

| Action | Method | Description |
| --- | --- | --- |
| [List questions](actions/list-questions.md) | GET | Retrieves agent questions from your Middesk account. |

### Registration Request

| Action | Method | Description |
| --- | --- | --- |
| [Create a registration request](actions/create-registration-request.md) | POST | Creates a registration request in Middesk. |
| [Delete a registration request](actions/delete-registration-request.md) | DELETE | Deletes a registration request from Middesk. |
| [Retrieve a registration request](actions/get-registration-request.md) | GET | Retrieves a registration request from Middesk. |
| [List registration requests](actions/list-registration-requests.md) | GET | Retrieves registration requests from your Middesk account. |

### Registration Request Guest Dashboard

| Action | Method | Description |
| --- | --- | --- |
| [Fetch guest dashboard link for a registration request](actions/get-registration-request-guest-dashboard.md) | GET | Retrieves a guest dashboard link from Middesk. |

### Related Business

| Action | Method | Description |
| --- | --- | --- |
| [List related businesses](actions/list-related-businesses.md) | GET | Retrieves related businesses from your Middesk account. |

### Signal

| Action | Method | Description |
| --- | --- | --- |
| [Create a signal](actions/create-signal.md) | POST | Creates a signal in your Middesk account. |
| [Retrieve a signal](actions/get-signal.md) | GET | Retrieves a signal from your Middesk account. |
| [List signals](actions/list-signals.md) | GET | Retrieves signals from your Middesk account. |

### Tin Match Availability

| Action | Method | Description |
| --- | --- | --- |
| [Get TIN Match Availability](actions/get-tin-match-availability.md) | GET | Retrieves TIN match availability from Middesk. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create a webhook](actions/create-webhook.md) | POST | Creates a webhook in your Middesk account. |
| [Delete a webhook](actions/delete-webhook.md) | DELETE | Deletes a webhook from your Middesk account. |
| [Retrieve a webhook](actions/get-webhook.md) | GET | Retrieves a webhook from your Middesk account. |
| [List webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from your Middesk account. |
| [Update a webhook](actions/update-webhook.md) | PUT | Updates a webhook in your Middesk account. |

