# <img src="https://images.mindcloud.co/apps/icons/icon_1774466672180.jpeg" alt="Salesforge logo" width="28" height="28"> Salesforge: Universal API

Manage outreach campaigns, mailboxes, and leads in Salesforge

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/salesforge/latest
- **Category:** Marketing
- **Actions:** 36
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.salesforge.ai
- **Vendor API docs:** https://api.salesforge.ai/public/v2/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Contact](actions/get-contact.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/get-contact?connectionId=$CONNECTION_ID&workspaceId=wks_lxxtq91neaixc8yaiqp7w&contactId=lead_n539nxku3oq5k3w1cc5py" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (36)

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Create Contacts](actions/bulk-create-contacts.md) | POST | Creates contacts in bulk in Salesforge. |
| [Create Contact](actions/create-contact.md) | POST | Creates a contact in Salesforge. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Salesforge. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Salesforge. |

### Custom Variable

| Action | Method | Description |
| --- | --- | --- |
| [List Custom Variables](actions/list-custom-variables.md) | GET | Retrieves custom variables from Salesforge. |

### Dnc

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Create DNCs](actions/bulk-create-dncs.md) | POST | Creates DNC entries in bulk in Salesforge. |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [Import Lead To Sequence](actions/import-lead-to-sequence.md) | POST | Imports a lead to a sequence in Salesforge. |

### Mailbox

| Action | Method | Description |
| --- | --- | --- |
| [List Mailboxes](actions/list-mailboxes.md) | GET | Retrieves mailboxes from Salesforge. |

### Primebox Label

| Action | Method | Description |
| --- | --- | --- |
| [List Primebox Labels](actions/list-primebox-labels.md) | GET | Retrieves Primebox labels from Salesforge. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a product in Salesforge. |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from Salesforge. |
| [List Products](actions/list-products.md) | GET | Retrieves products from Salesforge. |

### Sequence

| Action | Method | Description |
| --- | --- | --- |
| [Create Sequence](actions/create-sequence.md) | POST | Creates a sequence in Salesforge. |
| [Delete Sequence](actions/delete-sequence.md) | DELETE | Deletes a sequence from Salesforge. |
| [Get Sequence](actions/get-sequence.md) | GET | Retrieves a sequence from Salesforge. |
| [List Workspace Sequences](actions/list-workspace-sequences.md) | GET | Retrieves workspace sequences from Salesforge. |
| [Update Sequence](actions/update-sequence.md) | PUT | Updates a sequence in Salesforge. |
| [Update Sequence Status](actions/update-sequence-status.md) | PUT | Updates sequence status in Salesforge. |

### Sequence Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Sequence Analytics](actions/get-sequence-analytics.md) | GET | Retrieves sequence analytics from Salesforge. |

### Sequence Contact Assignment

| Action | Method | Description |
| --- | --- | --- |
| [Assign Contacts To Sequence](actions/assign-contacts-to-sequence.md) | PUT | Assigns contacts to a sequence in Salesforge. |

### Sequence Contact Sending Data

| Action | Method | Description |
| --- | --- | --- |
| [Get Sequence Contact Sending Data](actions/get-sequence-contact-sending-data.md) | GET | Retrieves sequence contact sending data from Salesforge. |

### Sequence Contact Validation

| Action | Method | Description |
| --- | --- | --- |
| [Start Sequence Contact Validation](actions/start-sequence-contact-validation.md) | PUT | Starts sequence contact validation in Salesforge. |

### Sequence Contact Validation Result

| Action | Method | Description |
| --- | --- | --- |
| [Confirm Sequence Contact Validation Results](actions/confirm-sequence-contact-validation-results.md) | PUT | Confirms sequence contact validation results in Salesforge. |
| [Get Sequence Contact Validation Results](actions/get-sequence-contact-validation-results.md) | GET | Retrieves sequence contact validation results from Salesforge. |
| [Skip Sequence Contact Validation Results](actions/skip-sequence-contact-validation-results.md) | PUT | Skips sequence contact validation results in Salesforge. |

### Sequence Contacts Count

| Action | Method | Description |
| --- | --- | --- |
| [Get Sequence Contacts Count](actions/get-sequence-contacts-count.md) | GET | Retrieves a sequence contacts count from Salesforge. |

### Sequence Schedule

| Action | Method | Description |
| --- | --- | --- |
| [Update Sequence Schedules](actions/update-sequence-schedules.md) | PUT | Updates sequence schedules in Salesforge. |

### Sequence Step

| Action | Method | Description |
| --- | --- | --- |
| [Update Sequence Steps](actions/update-sequence-steps.md) | PUT | Updates sequence steps in Salesforge. |

### Thread

| Action | Method | Description |
| --- | --- | --- |
| [List Workspace Threads](actions/list-workspace-threads.md) | GET | Retrieves workspace threads from Salesforge. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a webhook in Salesforge. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a webhook from Salesforge. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from Salesforge. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Create Workspace](actions/create-workspace.md) | POST | Creates a workspace in Salesforge. |
| [Get Workspace](actions/get-workspace.md) | GET | Retrieves a workspace from Salesforge. |
| [List Workspaces](actions/list-workspaces.md) | GET | Retrieves workspaces from Salesforge. |

### Workspace Sequence Metrics

| Action | Method | Description |
| --- | --- | --- |
| [Get Workspace Sequence Metrics](actions/get-workspace-sequence-metrics.md) | GET | Retrieves workspace sequence metrics from Salesforge. |

