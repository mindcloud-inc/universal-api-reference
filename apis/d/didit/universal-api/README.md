# <img src="https://images.mindcloud.co/apps/icons/didit_1774882981560.png" alt="Didit logo" width="28" height="28"> Didit: Universal API

Create verification workflows, run checks, and manage Didit sessions

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/didit/latest
- **Category:** IT Operations / Security & Identity
- **Actions:** 44
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://didit.me
- **Vendor API docs:** https://docs.didit.me/api-reference/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Sessions](actions/list-sessions.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/didit/latest/actions/list-sessions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (44)

### Approvals

| Action | Method | Description |
| --- | --- | --- |
| [Create Session Review](actions/create-session-review.md) | POST | Creates a new review for a session in Didit. |
| [List Session Reviews](actions/list-session-reviews.md) | GET | Retrieves reviews for a session from Didit. |

### Collections

| Action | Method | Description |
| --- | --- | --- |
| [Add to Blocklist](actions/add-to-blocklist.md) | POST | Adds an entry to the Didit blocklist. |
| [List Blocklist](actions/list-blocklist.md) | GET | Retrieves blocklist entries from Didit. |
| [Remove from Blocklist](actions/remove-from-blocklist.md) | DELETE | Removes an entry from the Didit blocklist. |

### Emails

| Action | Method | Description |
| --- | --- | --- |
| [Check Email Code](actions/check-email-code.md) | POST | Checks an email verification code in Didit. |
| [Send Email Code](actions/send-email-code.md) | POST | Sends an email verification code in Didit. |

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [Create Questionnaire](actions/create-questionnaire.md) | POST | Creates a new questionnaire in Didit. |
| [Delete Questionnaire](actions/delete-questionnaire.md) | DELETE | Deletes a questionnaire from Didit. |
| [Get Questionnaire](actions/get-questionnaire.md) | GET | Retrieves a questionnaire from Didit. |
| [List Questionnaires](actions/list-questionnaires.md) | GET | Retrieves questionnaires from Didit. |
| [Update Questionnaire](actions/update-questionnaire.md) | PUT | Updates an existing questionnaire in Didit. |

### Payments

| Action | Method | Description |
| --- | --- | --- |
| [Get Credit Balance](actions/get-credit-balance.md) | GET | Retrieves the credit balance from Didit. |
| [Top Up Credits](actions/top-up-credits.md) | POST | Creates a credit top-up request in Didit. |

### Phone Numbers

| Action | Method | Description |
| --- | --- | --- |
| [Check Phone Code](actions/check-phone-code.md) | POST | Checks a phone verification code in Didit. |
| [Send Phone Code](actions/send-phone-code.md) | POST | Sends a phone verification code in Didit. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Age Estimation](actions/age-estimation.md) | POST | Creates an age estimation report in Didit. |
| [AML Screening](actions/aml-screening.md) | POST | Creates an AML screening report in Didit. |
| [Database Validation](actions/database-validation.md) | POST | Creates a database validation report in Didit. |
| [Face Match](actions/face-match.md) | POST | Creates a face match report in Didit. |
| [Face Search](actions/face-search.md) | POST | Creates a face search report in Didit. |
| [ID Verification](actions/id-verification.md) | POST | Creates an ID verification report in Didit. |
| [Passive Liveness](actions/passive-liveness.md) | POST | Creates a passive liveness report in Didit. |
| [Proof of Address](actions/proof-of-address.md) | POST | Creates a proof of address report in Didit. |

### Session

| Action | Method | Description |
| --- | --- | --- |
| [Create Session](actions/create-session.md) | POST | Creates a new verification session in Didit. |
| [Delete Session](actions/delete-session.md) | DELETE | Deletes a session from Didit. |
| [Generate Session PDF](actions/generate-session-pdf.md) | GET | Retrieves a session PDF report from Didit. |
| [Import Shared Session](actions/import-shared-session.md) | POST | Imports a shared session into Didit. |
| [List Sessions](actions/list-sessions.md) | GET | Retrieves sessions from Didit. |
| [Retrieve Session](actions/retrieve-session.md) | GET | Retrieves a session decision from Didit. |
| [Share Session](actions/share-session.md) | POST | Creates a share token for a session in Didit. |
| [Update Session Status](actions/update-session-status.md) | PUT | Updates a session status in Didit. |

### Sessions

| Action | Method | Description |
| --- | --- | --- |
| [Batch Delete Sessions](actions/batch-delete-sessions.md) | DELETE | Deletes multiple sessions from Didit. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Batch Delete Users](actions/batch-delete-users.md) | DELETE | Deletes multiple users from Didit. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Didit. |
| [List Users](actions/list-users.md) | GET | Retrieves users from Didit. |
| [Update User](actions/update-user.md) | PUT | Updates an existing user in Didit. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Get Webhook Configuration](actions/get-webhook-configuration.md) | GET | Retrieves the webhook configuration from Didit. |
| [Update Webhook Configuration](actions/update-webhook-configuration.md) | PUT | Updates the webhook configuration in Didit. |

### Workflow

| Action | Method | Description |
| --- | --- | --- |
| [Create Workflow](actions/create-workflow.md) | POST | Creates a new workflow in Didit. |
| [Delete Workflow](actions/delete-workflow.md) | DELETE | Deletes a workflow from Didit. |
| [Get Workflow](actions/get-workflow.md) | GET | Retrieves a workflow from Didit. |
| [List Workflows](actions/list-workflows.md) | GET | Retrieves workflows from Didit. |
| [Update Workflow](actions/update-workflow.md) | PUT | Updates an existing workflow in Didit. |

