# <img src="https://images.mindcloud.co/apps/icons/uni-one_1774973620451.png" alt="UniOne logo" width="28" height="28"> UniOne: Universal API

Send emails, manage domains and projects, and track delivery

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/uniOne/latest
- **Category:** Marketing
- **Actions:** 34
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://unione.io/
- **Vendor API docs:** https://docs.unione.io/en/web-api-ref

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get System Info](actions/get-system-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/get-system-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (34)

### Domain

| Action | Method | Description |
| --- | --- | --- |
| [Delete Domain](actions/delete-domain.md) | DELETE | Deletes an existing domain from UniOne. |
| [Get Domain DNS Records](actions/get-domain-dns-records.md) | GET | Retrieves domain DNS records from UniOne. |
| [List Domains](actions/list-domains.md) | GET | Retrieves domains from UniOne, optionally by exact domain. |
| [Validate DKIM](actions/validate-dkim.md) | GET | Validates DKIM records for a domain in UniOne. |
| [Validate Domain Verification Record](actions/validate-domain-verification-record.md) | GET | Validates a domain verification record in UniOne. |

### Email

| Action | Method | Description |
| --- | --- | --- |
| [Send Email](actions/send-email.md) | POST | Sends an email message through UniOne. |
| [Subscribe Email](actions/subscribe-email.md) | POST | Subscribes an email address through UniOne. |

### Email Validation

| Action | Method | Description |
| --- | --- | --- |
| [Validate Single Email](actions/validate-single-email.md) | GET | Validates a single email address in UniOne. |

### Event Dump Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Event Dump Job](actions/create-event-dump-job.md) | POST | Creates an event dump job in UniOne. |
| [Delete Event Dump Job](actions/delete-event-dump-job.md) | DELETE | Deletes an event dump job from UniOne. |
| [Get Event Dump Job](actions/get-event-dump-job.md) | GET | Retrieves an event dump job from UniOne. |
| [List Event Dump Jobs](actions/list-event-dump-jobs.md) | GET | Retrieves event dump jobs from UniOne. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in UniOne. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes an existing project from UniOne. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from UniOne, optionally by project ID. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in UniOne. |

### Suppression

| Action | Method | Description |
| --- | --- | --- |
| [Add Suppression](actions/add-suppression.md) | POST | Adds an email address to UniOne's suppression list. |
| [Delete Suppression](actions/delete-suppression.md) | DELETE | Deletes a suppression from UniOne by email address. |
| [Get Suppression](actions/get-suppression.md) | GET | Retrieves suppression details from UniOne by email address. |
| [List Suppressions](actions/list-suppressions.md) | GET | Retrieves suppressions from UniOne with optional filters. |

### System

| Action | Method | Description |
| --- | --- | --- |
| [Get System Info](actions/get-system-info.md) | GET | Retrieves account and usage details from UniOne. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Delete Tag](actions/delete-tag.md) | DELETE | Deletes an existing tag from UniOne. |
| [List Tags](actions/list-tags.md) | GET | Retrieves all saved tags from UniOne. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Create Or Update Template](actions/create-or-update-template.md) | POST | Creates or updates an email template in UniOne. |
| [Delete Template](actions/delete-template.md) | DELETE | Deletes an email template from UniOne by ID. |
| [Get Template](actions/get-template.md) | GET | Retrieves an email template from UniOne by ID. |
| [List Templates](actions/list-templates.md) | GET | Retrieves email templates from UniOne, optionally by name. |

### Unsubscribed Email

| Action | Method | Description |
| --- | --- | --- |
| [Check Unsubscribed](actions/check-unsubscribed.md) | GET | Checks whether an email address is unsubscribed in UniOne. |
| [List Unsubscribed](actions/list-unsubscribed.md) | GET | Retrieves unsubscribed email addresses from UniOne. |
| [Set Unsubscribed](actions/set-unsubscribed.md) | POST | Adds an email address to UniOne's unsubscribed list. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Or Update Webhook](actions/create-or-update-webhook.md) | POST | Creates or updates a webhook in UniOne. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes a webhook from UniOne by URL. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a webhook from UniOne by URL. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves configured webhooks from UniOne for the account. |

