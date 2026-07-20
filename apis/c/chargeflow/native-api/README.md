# Chargeflow: Native API Reference

A consolidated summary of Chargeflow's API configuration and 34 documented operations, with links to official documentation.

- **Official docs:** https://docs.chargeflow.io/reference/api-overview
- **API base URL:** `https://api.chargeflow.io/public/2025-04-01`

## Authentication

### API Key

Use your Chargeflow API key. HMAC signing is optional and is not required for the default wrapper path in this run.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://docs.chargeflow.io/docs/getting-started#authentication)

## Endpoints (34 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Account](actions/create-account.md) | `POST /accounts` | [docs](https://docs.chargeflow.io/reference/post_public-2025-04-01-accounts-1) |
| [Create Customer Communication](actions/create-customer-communication.md) | `POST /customer-communication` | [docs](https://docs.chargeflow.io/reference/post_public-2025-04-01-customer-communication) |
| [Create Data Subject Removal Request](actions/create-data-subject-removal-request.md) | `POST /data-subject/removal` | [docs](https://docs.chargeflow.io/reference/post_public-2025-04-01-data-subject-removal) |
| [Create Dispute](actions/create-dispute.md) | `POST /platform/disputes` | [docs](https://docs.chargeflow.io/reference/post_public-2025-04-01-platform-disputes-1) |
| [Create Integration](actions/create-integration.md) | `POST /integrations` | [docs](https://docs.chargeflow.io/reference/post_public-2025-04-01-integrations-1) |
| [Create Order](actions/create-order.md) | `POST /{disputeId}/order` | [docs](https://docs.chargeflow.io/reference/post_public-2025-04-01-disputeid-order-1) |
| [Create Subscription](actions/create-subscription.md) | `POST /disputes/{disputeId}/subscription` | [docs](https://docs.chargeflow.io/reference/post_public-2025-04-01-disputes-disputeid-subscription-1) |
| [Create Transaction](actions/create-transaction.md) | `POST /disputes/{disputeId}/transaction` | [docs](https://docs.chargeflow.io/reference/transaction) |
| [Create User Event Log](actions/create-user-event-log.md) | `POST /disputes/{disputeId}/user_events_log` | [docs](https://docs.chargeflow.io/reference/post_public-2025-04-01-disputes-disputeid-user-events-log-1) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://docs.chargeflow.io/reference/post_public-2025-04-01-webhooks-1) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhooks/{id}` | [docs](https://docs.chargeflow.io/reference/delete_public-2025-04-01-webhooks-id-1) |
| [Enrich Dispute](actions/enrich-dispute.md) | `PATCH /disputes/{disputeId}` | [docs](https://docs.chargeflow.io/reference/patch_public-2025-04-01-disputes-disputeid-1) |
| [Generate Evidence](actions/generate-evidence.md) | `POST /evidence` | [docs](https://docs.chargeflow.io/reference/post_public-2025-04-01-evidence) |
| [Get Account By ID](actions/get-account-by-id.md) | `GET /accounts/{accountId}` | [docs](https://docs.chargeflow.io/reference/get_public-2025-04-01-accounts-accountid-1) |
| [Get Alert By ID](actions/get-alert-by-id.md) | `GET /alerts/{alertId}` | [docs](https://docs.chargeflow.io/reference/get_public-2025-04-01-alerts-alertid-1) |
| [Get Dispute By ID](actions/get-dispute-by-id.md) | `GET /disputes/{disputeId}` | [docs](https://docs.chargeflow.io/reference/get_public-2025-04-01-disputes-disputeid-1) |
| [Get Evidence By ID](actions/get-evidence-by-id.md) | `GET /evidence/{evidenceId}` | [docs](https://docs.chargeflow.io/reference/get_public-2025-04-01-evidence-evidenceid) |
| [Get Integration By ID](actions/get-integration-by-id.md) | `GET /integrations/{integrationId}` | [docs](https://docs.chargeflow.io/reference/put_public-2025-04-01-integrations-integrationid-1) |
| [Get Removal Request Status](actions/get-removal-request-status.md) | `GET /data-subject/removal/{requestId}` | [docs](https://docs.chargeflow.io/reference/get_public-2025-04-01-data-subject-removal-requestid) |
| [List Accounts](actions/list-accounts.md) | `GET /accounts` | [docs](https://docs.chargeflow.io/reference/get_public-2025-04-01-accounts-1) |
| [List Alerts](actions/list-alerts.md) | `GET /alerts` | [docs](https://docs.chargeflow.io/reference/get_public-2025-04-01-alerts-1) |
| [List Disputes](actions/list-disputes.md) | `GET /disputes` | [docs](https://docs.chargeflow.io/reference/get_public-2025-04-01-disputes-1) |
| [List Evidence](actions/list-evidence.md) | `GET /evidence` | [docs](https://docs.chargeflow.io/reference/get_public-2025-04-01-evidence) |
| [List Integrations](actions/list-integrations.md) | `GET /integrations` | [docs](https://docs.chargeflow.io/reference/get_public-2025-04-01-integrations-1) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://docs.chargeflow.io/reference/get_public-2025-04-01-webhooks-1) |
| [Revoke Integration Access](actions/revoke-integration-access.md) | `DELETE /integrations/{integrationId}` | [docs](https://docs.chargeflow.io/reference/delete_public-2025-04-01-integrations-integrationid-1) |
| [Update Account](actions/update-account.md) | `PATCH /accounts/{accountId}` | [docs](https://docs.chargeflow.io/reference/patch_public-2025-04-01-accounts-accountid-1) |
| [Update Alert Outcome](actions/update-alert-outcome.md) | `POST /alerts/{alertId}/outcome` | [docs](https://docs.chargeflow.io/reference/post_public-2025-04-01-alerts-alertid-outcome) |
| [Update Dispute Order](actions/update-dispute-order.md) | `POST /disputes/{disputeId}/order` | [docs](https://docs.chargeflow.io/reference/post_public-2025-04-01-disputes-disputeid-order-1) |
| [Update Integration](actions/update-integration.md) | `PUT /integrations/{integrationId}` | [docs](https://docs.chargeflow.io/reference/put_public-2025-04-01-integrations-integrationid-1) |
| [Upload Evidence](actions/upload-evidence.md) | `POST /disputes/{disputeId}/evidence` | [docs](https://docs.chargeflow.io/reference/post_public-2025-04-01-disputes-disputeid-evidence-1) |
| [Validate Access Key](actions/validate-access-key.md) | `POST /health-check/access-key` |  |
| [Verify Access Key](actions/verify-access-key.md) | `GET /health-check/access-key` | [docs](https://docs.chargeflow.io/reference/get_public-2025-04-01-health-check-access-key-1) |
| [Verify Service Health](actions/verify-service-health.md) | `GET /health-check` | [docs](https://docs.chargeflow.io/reference/get_public-2025-04-01-health-check-1) |
