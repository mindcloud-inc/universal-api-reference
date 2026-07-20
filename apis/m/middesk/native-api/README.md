# Middesk: Native API Reference

A consolidated summary of Middesk's API configuration and 68 documented operations, with links to official documentation.

- **Official docs:** https://docs.middesk.com/build/api-keys
- **OpenAPI specification:** https://docs.middesk.com/openapi.json
- **API base URL:** `https://api.middesk.com/v1`

## Authentication

### API Key

Authenticate to Middesk using a live API key sent as a bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.middesk.com/build/api-keys)

## API conventions

The total page count is read from `input.total_count`.

## Endpoints (68 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Autocomplete business identities](actions/autocomplete-business-identities.md) | `POST /identities/autocomplete` | [docs](https://docs.middesk.com/reference/businesses) |
| [Bulk disable monitors](actions/bulk-disable-monitors.md) | `POST /monitoring/bulk_disable` | [docs](https://docs.middesk.com/reference/businesses) |
| [Prefill business information](actions/business.md) | `POST /prefill/businesses` | [docs](https://docs.middesk.com/reference/businesses) |
| [Create an action on an object](actions/create-action.md) | `POST /actions` | [docs](https://docs.middesk.com/reference/introduction) |
| [Create an agent run](actions/create-agent-run.md) | `POST /runs` | [docs](https://docs.middesk.com/reference/introduction) |
| [Create an agent thread](actions/create-agent-thread.md) | `POST /threads` | [docs](https://docs.middesk.com/reference/introduction) |
| [Create an application](actions/create-application.md) | `POST /partner/applications` | [docs](https://docs.middesk.com/docs/jurisdiction-registration-flow) |
| [Create a business](actions/create-business.md) | `POST /businesses` | [docs](https://docs.middesk.com/reference/introduction) |
| [Create a business batch](actions/create-business-batch.md) | `POST /business_batches` | [docs](https://docs.middesk.com/reference/businesses) |
| [Create a monitor for a business](actions/create-business-monitor.md) | `POST /businesses/:business_id/monitor` | [docs](https://docs.middesk.com/reference/businesses) |
| [Create a company](actions/create-company.md) | `POST /partner/companies` | [docs](https://docs.middesk.com/docs/jurisdiction-registration-flow) |
| [Create a lien for a business](actions/create-lien.md) | `POST /businesses/:business_id/liens` | [docs](https://docs.middesk.com/reference/businesses) |
| [Create lien filings in batch](actions/create-lien-filings-in-batch.md) | `POST /businesses/:business_id/liens/batch` | [docs](https://docs.middesk.com/reference/businesses) |
| [Create a termination for a lien](actions/create-lien-termination.md) | `POST /liens/:lien_id/termination` | [docs](https://docs.middesk.com/reference/businesses) |
| [Create an order for a business](actions/create-order.md) | `POST /businesses/:business_id/orders` | [docs](https://docs.middesk.com/reference/order) |
| [Create a registration request](actions/create-registration-request.md) | `POST /partner/registration_requests` | [docs](https://docs.middesk.com/docs/jurisdiction-registration-flow) |
| [Create a signal](actions/create-signal.md) | `POST /signals` | [docs](https://docs.middesk.com/reference/introduction) |
| [Create a webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://docs.middesk.com/reference/webhooks) |
| [Delete a monitor for a business](actions/delete-business-monitor.md) | `DELETE /businesses/:business_id/monitor` | [docs](https://docs.middesk.com/reference/businesses) |
| [Delete a registration request](actions/delete-registration-request.md) | `DELETE /partner/registration_requests/:id` | [docs](https://docs.middesk.com/docs/jurisdiction-registration-flow) |
| [Delete a webhook](actions/delete-webhook.md) | `DELETE /webhooks/:id` | [docs](https://docs.middesk.com/reference/webhooks) |
| [Retrieve an action](actions/get-action.md) | `GET /actions/:id` | [docs](https://docs.middesk.com/reference/introduction) |
| [Retrieve an agent](actions/get-agent.md) | `GET /agents/:id` | [docs](https://docs.middesk.com/reference/introduction) |
| [Retrieve an agent run](actions/get-agent-run.md) | `GET /runs/:id` | [docs](https://docs.middesk.com/reference/introduction) |
| [Retrieve an agent thread](actions/get-agent-thread.md) | `GET /threads/:id` | [docs](https://docs.middesk.com/reference/introduction) |
| [Retrieve a business](actions/get-business.md) | `GET /businesses/:id` | [docs](https://docs.middesk.com/reference/introduction) |
| [Retrieve a business batch](actions/get-business-batch.md) | `GET /business_batches/:id` | [docs](https://docs.middesk.com/reference/businesses) |
| [Download business batch CSV](actions/get-business-batch-csv.md) | `GET /business_batches/:id/csv` | [docs](https://docs.middesk.com/reference/businesses) |
| [Retrieve a monitor for a business](actions/get-business-monitor.md) | `GET /businesses/:business_id/monitor` | [docs](https://docs.middesk.com/reference/businesses) |
| [Retrieve a business PDF](actions/get-business-pdf.md) | `GET /businesses/:id/pdf` | [docs](https://docs.middesk.com/reference/businesses) |
| [Retrieve a review for a business](actions/get-business-review.md) | `GET /businesses/:business_id/review` | [docs](https://docs.middesk.com/reference/businesses) |
| [Retrieve timeline for a business](actions/get-business-timeline.md) | `GET /businesses/:business_id/timeline` | [docs](https://docs.middesk.com/reference/businesses) |
| [Retrieve website analysis for a business](actions/get-business-website.md) | `GET /businesses/:business_id/website` | [docs](https://docs.middesk.com/reference/businesses) |
| [Get a document](actions/get-document.md) | `GET /documents/:id` | [docs](https://docs.middesk.com/reference/document) |
| [Get document download URL](actions/get-document-download-url.md) | `GET /documents/:id/download_url` | [docs](https://docs.middesk.com/reference/document) |
| [Retrieve a mail item](actions/get-mail-item.md) | `GET /partner/mail/:id` | [docs](https://docs.middesk.com/reference/agent-mail) |
| [Retrieve OIDC public keys](actions/get-oidc-keys.md) | `GET /webhooks/oidc_keys` | [docs](https://docs.middesk.com/reference/webhooks) |
| [Retrieve an order](actions/get-order.md) | `GET /businesses/:business_id/orders/:id` | [docs](https://docs.middesk.com/reference/order) |
| [Retrieve an order by ID](actions/get-order-by-id.md) | `GET /orders/:id` | [docs](https://docs.middesk.com/reference/order) |
| [Retrieve a registration request](actions/get-registration-request.md) | `GET /partner/registration_requests/:id` | [docs](https://docs.middesk.com/docs/jurisdiction-registration-flow) |
| [Fetch guest dashboard link for a registration request](actions/get-registration-request-guest-dashboard.md) | `GET /partner/registration_requests/:id/guest_dashboard` | [docs](https://docs.middesk.com/docs/jurisdiction-registration-flow) |
| [Retrieve a signal](actions/get-signal.md) | `GET /signals/:id` | [docs](https://docs.middesk.com/reference/introduction) |
| [Get TIN Match Availability](actions/get-tin-match-availability.md) | `GET /tin_match/availability` | [docs](https://docs.middesk.com/reference/tin-match) |
| [Retrieve a webhook](actions/get-webhook.md) | `GET /webhooks/:id` | [docs](https://docs.middesk.com/reference/webhooks) |
| [List actions for an object](actions/list-actions.md) | `GET /actions` | [docs](https://docs.middesk.com/reference/introduction) |
| [List agent runs](actions/list-agent-runs.md) | `GET /runs` | [docs](https://docs.middesk.com/reference/introduction) |
| [List agent threads](actions/list-agent-threads.md) | `GET /threads` | [docs](https://docs.middesk.com/reference/introduction) |
| [List agents](actions/list-agents.md) | `GET /agents` | [docs](https://docs.middesk.com/reference/introduction) |
| [List business batches](actions/list-business-batches.md) | `GET /business_batches` | [docs](https://docs.middesk.com/reference/businesses) |
| [List policy results for a business](actions/list-business-policy-results.md) | `GET /businesses/:business_id/policy_results` | [docs](https://docs.middesk.com/reference/businesses) |
| [List Businesses](actions/list-businesses.md) | `GET /businesses` | [docs](https://docs.middesk.com/reference/introduction) |
| [List documents for a business](actions/list-documents.md) | `GET /businesses/:business_id/documents` | [docs](https://docs.middesk.com/reference/document) |
| [List Information Requests](actions/list-information-requests.md) | `GET /partner/exceptions` | [docs](https://docs.middesk.com/reference/agent-mail) |
| [Fetch supported local jurisdictions](actions/list-jurisdictions.md) | `GET /agent/jurisdictions` | [docs](https://docs.middesk.com/docs/jurisdiction-registration-flow) |
| [List liens for a business](actions/list-liens.md) | `GET /businesses/:business_id/liens` | [docs](https://docs.middesk.com/reference/businesses) |
| [List mail items](actions/list-mail-items.md) | `GET /partner/mail` | [docs](https://docs.middesk.com/reference/agent-mail) |
| [List orders for a business](actions/list-orders.md) | `GET /businesses/:business_id/orders` | [docs](https://docs.middesk.com/reference/order) |
| [List questions](actions/list-questions.md) | `GET /agent/questions` | [docs](https://docs.middesk.com/work-with-agents/run-agents) |
| [List registration requests](actions/list-registration-requests.md) | `GET /partner/registration_requests` | [docs](https://docs.middesk.com/docs/jurisdiction-registration-flow) |
| [List related businesses](actions/list-related-businesses.md) | `GET /businesses/:business_id/related_businesses` | [docs](https://docs.middesk.com/reference/businesses) |
| [List signals](actions/list-signals.md) | `GET /signals` | [docs](https://docs.middesk.com/reference/introduction) |
| [List webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://docs.middesk.com/reference/webhooks) |
| [Stream agent run events](actions/stream-agent-run-events.md) | `GET /runs/:id/stream` | [docs](https://docs.middesk.com/reference/introduction) |
| [Update a business](actions/update-business.md) | `PATCH /businesses/:id` | [docs](https://docs.middesk.com/reference/introduction) |
| [Update a monitor for a business](actions/update-business-monitor.md) | `PUT /businesses/:business_id/monitor` | [docs](https://docs.middesk.com/reference/businesses) |
| [Update a mail item](actions/update-mail-item.md) | `PATCH /partner/mail/:id` | [docs](https://docs.middesk.com/reference/agent-mail) |
| [Update an order](actions/update-order.md) | `PUT /orders/:id` | [docs](https://docs.middesk.com/reference/order) |
| [Update a webhook](actions/update-webhook.md) | `PUT /webhooks/:id` | [docs](https://docs.middesk.com/reference/webhooks) |
