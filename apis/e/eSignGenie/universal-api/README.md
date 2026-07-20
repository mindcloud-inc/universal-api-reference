# <img src="https://images.mindcloud.co/apps/icons/e-sign-genie_1774900274148.png" alt="eSign Genie logo" width="28" height="28"> eSign Genie: Universal API

Manage Foxit eSign envelopes, templates, webhooks, reports, and user administration from the Foxit eSign API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/eSignGenie/latest
- **Category:** Productivity / Legal & Contracts
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.foxit.com/api/esign-api/
- **Vendor API docs:** https://docs.developer-api.foxit.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List All Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eSignGenie/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Download Single Document PDF](actions/download-single-document-pdf.md) | GET | Retrieves a document PDF from eSign Genie. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Download Report](actions/download-report.md) | GET | Retrieves an envelope report from eSign Genie. |

### Signature Requests

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Envelope](actions/cancel-envelope.md) | PUT | Cancels an envelope in eSign Genie. |
| [Create Envelope from Template](actions/create-envelope-from-template.md) | POST | Creates a new envelope from a template in eSign Genie. |
| [Create Envelope from URL](actions/create-envelope-from-url.md) | POST | Creates a new envelope from document URLs in eSign Genie. |
| [Delete Envelopes](actions/delete-envelopes.md) | DELETE | Deletes envelopes from eSign Genie. |
| [Download Envelope Files](actions/download-envelope-files.md) | GET | Retrieves envelope files from eSign Genie. |
| [Get Envelope Activity History](actions/get-envelope-activity-history.md) | GET | Retrieves envelope activity history from eSign Genie. |
| [Get Envelope Details](actions/get-envelope-details.md) | GET | Retrieves envelope details from eSign Genie. |
| [Get Envelope Ids](actions/get-envelope-ids.md) | GET | Retrieves envelope IDs from eSign Genie. |
| [Modify Shared Envelope](actions/modify-shared-envelope.md) | PUT | Updates a shared envelope in eSign Genie. |
| [Move Envelopes to Recycle Bin](actions/move-envelopes-to-recycle-bin.md) | DELETE | Moves envelopes to the recycle bin in eSign Genie. |
| [Send Draft Envelope](actions/send-draft-envelope.md) | PUT | Sends a draft envelope in eSign Genie. |
| [Send Signature Reminder](actions/send-signature-reminder.md) | PUT | Sends a signature reminder from eSign Genie. |
| [Update Envelope Fields](actions/update-envelope-fields.md) | PUT | Updates envelope fields in eSign Genie. |
| [Update Envelope Recipients](actions/update-envelope-recipients.md) | PUT | Updates envelope recipients in eSign Genie. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [Create Template from URL](actions/create-template-from-url.md) | POST | Creates a new template from document URLs in eSign Genie. |
| [Get a List of All Templates](actions/get-a-list-of-all-templates.md) | GET | Retrieves templates from eSign Genie. |
| [Get Template Details](actions/get-template-details.md) | GET | Retrieves template details from eSign Genie. |
| [Get Templates by Template IDs](actions/get-templates-by-template-i-ds.md) | GET | Retrieves templates from eSign Genie by template ID. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a new user in eSign Genie. |
| [List All Users](actions/list-users.md) | GET | Retrieves users from eSign Genie. |
| [Update User](actions/update-user.md) | PUT | Updates an existing user in eSign Genie. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook Channel](actions/create-webhook-channel.md) | POST | Creates a new webhook channel in eSign Genie. |
| [Deactivate Webhook Channel](actions/deactivate-webhook-channel.md) | PUT | Deactivates a webhook channel in eSign Genie. |
| [Delete Webhook Channel](actions/delete-webhook-channel.md) | DELETE | Deletes a webhook channel from eSign Genie. |
| [Get Webhook Channel Details](actions/get-webhook-channel-details.md) | GET | Retrieves webhook channel details from eSign Genie. |
| [List All Webhook Channels](actions/list-all-webhook-channels.md) | GET | Retrieves webhook channels from eSign Genie. |
| [Reactivate Webhook Channel](actions/reactivate-webhook-channel.md) | PUT | Reactivates a webhook channel in eSign Genie. |
| [Update Webhook Channel](actions/update-webhook-channel.md) | PUT | Updates an existing webhook channel in eSign Genie. |

