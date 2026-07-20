# <img src="https://images.mindcloud.co/apps/icons/chargeflow_1774894191987.png" alt="Chargeflow logo" width="28" height="28"> Chargeflow: Universal API

Automate chargebacks, alerts, disputes, webhooks, evidence generation, and Chargeflow Connect account operations through the Chargeflow public API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/chargeflow/latest
- **Category:** Commerce
- **Actions:** 34
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.chargeflow.io/
- **Vendor API docs:** https://docs.chargeflow.io/reference/api-overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Verify Access Key](actions/verify-access-key.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeflow/latest/actions/verify-access-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (34)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Create Account](actions/create-account.md) | POST | Creates a new Chargeflow Connect account. |
| [Get Account By ID](actions/get-account-by-id.md) | GET | Retrieves an existing Chargeflow Connect account. |
| [List Accounts](actions/list-accounts.md) | GET | Retrieves Chargeflow Connect accounts from your workspace. |
| [Update Account](actions/update-account.md) | PUT | Updates an existing Chargeflow Connect account. |

### Alert

| Action | Method | Description |
| --- | --- | --- |
| [Get Alert By ID](actions/get-alert-by-id.md) | GET | Retrieves an existing alert from Chargeflow. |
| [List Alerts](actions/list-alerts.md) | GET | Retrieves alerts from your Chargeflow account. |
| [Update Alert Outcome](actions/update-alert-outcome.md) | PUT | Updates an existing alert outcome in Chargeflow. |

### Customer Communication

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer Communication](actions/create-customer-communication.md) | POST | Creates customer communication records in Chargeflow. |

### Data Subject Removal Request

| Action | Method | Description |
| --- | --- | --- |
| [Create Data Subject Removal Request](actions/create-data-subject-removal-request.md) | POST | Creates a data subject removal request in Chargeflow. |
| [Get Removal Request Status](actions/get-removal-request-status.md) | GET | Retrieves a data removal request status from Chargeflow. |

### Dispute

| Action | Method | Description |
| --- | --- | --- |
| [Enrich Dispute](actions/enrich-dispute.md) | PUT | Enriches an existing dispute in Chargeflow. |
| [Get Dispute By ID](actions/get-dispute-by-id.md) | GET | Retrieves an existing dispute from Chargeflow. |
| [List Disputes](actions/list-disputes.md) | GET | Retrieves disputes from your Chargeflow account. |
| [Update Dispute Order](actions/update-dispute-order.md) | PUT | Updates dispute order details in Chargeflow. |
| [Upload Evidence](actions/upload-evidence.md) | POST | Uploads evidence for an existing dispute in Chargeflow. |

### Evidence

| Action | Method | Description |
| --- | --- | --- |
| [Generate Evidence](actions/generate-evidence.md) | POST | Generates evidence for an existing dispute in Chargeflow. |
| [Get Evidence By ID](actions/get-evidence-by-id.md) | GET | Retrieves existing dispute evidence from Chargeflow. |
| [List Evidence](actions/list-evidence.md) | GET | Retrieves dispute evidence from your Chargeflow account. |

### Health Check

| Action | Method | Description |
| --- | --- | --- |
| [Validate Access Key](actions/validate-access-key.md) | GET |  |
| [Verify Access Key](actions/verify-access-key.md) | GET | Verifies a Chargeflow API access key. |
| [Verify Service Health](actions/verify-service-health.md) | GET | Checks the current Chargeflow service health status. |

### Integration

| Action | Method | Description |
| --- | --- | --- |
| [Create Integration](actions/create-integration.md) | POST | Creates a new integration in Chargeflow. |
| [Get Integration By ID](actions/get-integration-by-id.md) | GET | Retrieves an existing integration from Chargeflow. |
| [List Integrations](actions/list-integrations.md) | GET | Retrieves integrations from your Chargeflow account. |
| [Revoke Integration Access](actions/revoke-integration-access.md) | DELETE | Revokes access for an existing Chargeflow integration. |
| [Update Integration](actions/update-integration.md) | PUT | Updates an existing integration in Chargeflow. |

### Merchant Dispute

| Action | Method | Description |
| --- | --- | --- |
| [Create Dispute](actions/create-dispute.md) | POST | Creates a new dispute in Chargeflow. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Order](actions/create-order.md) | POST | Creates a new dispute order in Chargeflow. |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Create Subscription](actions/create-subscription.md) | POST | Creates a new dispute subscription in Chargeflow. |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Create Transaction](actions/create-transaction.md) | POST | Creates a new dispute transaction in Chargeflow. |

### User Event Log

| Action | Method | Description |
| --- | --- | --- |
| [Create User Event Log](actions/create-user-event-log.md) | POST | Creates a user event log in Chargeflow. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Chargeflow. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from Chargeflow. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from your Chargeflow account. |

