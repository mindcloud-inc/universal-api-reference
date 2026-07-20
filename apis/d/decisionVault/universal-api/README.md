# <img src="https://images.mindcloud.co/apps/icons/decision-vault_1774470984794.png" alt="DecisionVault logo" width="28" height="28"> DecisionVault: Universal API

Manage DecisionVault matters, questionnaires, documents, and webhooks

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/decisionVault/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 17
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://decisionvault.com
- **Vendor API docs:** https://docs.decisionvault.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Matters](actions/list-matters.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/decisionVault/latest/actions/list-matters?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (17)

### Asset

| Action | Method | Description |
| --- | --- | --- |
| [List Assets for Matter](actions/list-assets-for-matter.md) | GET | Retrieves assets for a matter in DecisionVault. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [List Clients for Matter](actions/list-clients-for-matter.md) | GET | Retrieves clients for a matter in DecisionVault. |
| [List Contacts for Matter](actions/list-contacts-for-matter.md) | GET | Retrieves contacts for a matter in DecisionVault. |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Get Document](actions/get-document.md) | GET | Retrieves a document from DecisionVault by ID. |
| [List Documents for Matter](actions/list-documents-for-matter.md) | GET | Retrieves documents for a matter in DecisionVault. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Event](actions/get-event.md) | GET | Retrieves an event from DecisionVault by ID. |
| [List Events](actions/list-events.md) | GET | Retrieves events from your firm in DecisionVault. |

### Financial Category

| Action | Method | Description |
| --- | --- | --- |
| [List Financial Categories](actions/list-financial-categories.md) | GET | Retrieves financial categories available in DecisionVault. |

### Financial Document

| Action | Method | Description |
| --- | --- | --- |
| [List Financial Documents for Matter](actions/list-financial-documents-for-matter.md) | GET | Retrieves financial documents for a matter in DecisionVault. |

### Matter

| Action | Method | Description |
| --- | --- | --- |
| [Create Matter](actions/create-matter.md) | POST | Creates a matter in DecisionVault and returns an invite link. |
| [Get Matter](actions/get-matter.md) | GET | Retrieves a matter from DecisionVault by ID. |
| [List Matters](actions/list-matters.md) | GET | Retrieves matters from your firm in DecisionVault. |

### Questionnaire

| Action | Method | Description |
| --- | --- | --- |
| [Get Questionnaire](actions/get-questionnaire.md) | GET | Retrieves a questionnaire from DecisionVault by ID. |
| [List Questionnaires](actions/list-questionnaires.md) | GET | Retrieves questionnaires from your firm in DecisionVault. |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook Subscription](actions/create-webhook-subscription.md) | POST | Creates a webhook subscription in DecisionVault for an event type. |
| [Delete Webhook Subscription](actions/delete-webhook-subscription.md) | DELETE | Deletes a webhook subscription from DecisionVault. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves a user from DecisionVault by ID. |

