# <img src="https://images.mindcloud.co/apps/icons/feathery_1774012170112.png" alt="Feathery logo" width="28" height="28"> Feathery: Universal API

Build forms, collect submissions, and generate documents

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/feathery/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 28
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.feathery.io
- **Vendor API docs:** https://api-docs.feathery.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Retrieve Account Information](actions/retrieve-account-information.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/feathery/latest/actions/retrieve-account-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (28)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Edit Account](actions/edit-account.md) | PUT |  |
| [Invite Accounts](actions/invite-accounts.md) | POST |  |
| [Remove Account](actions/remove-account.md) | DELETE |  |
| [Retrieve Account Information](actions/retrieve-account-information.md) | GET |  |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Fill or Sign a Document Template](actions/fill-or-sign-a-document-template.md) | POST |  |
| [List Document Templates](actions/list-document-templates.md) | GET |  |

### Email

| Action | Method | Description |
| --- | --- | --- |
| [List Emails Sent From Form](actions/list-emails-sent-from-form.md) | GET |  |

### Email Issue

| Action | Method | Description |
| --- | --- | --- |
| [List Email Issues](actions/list-email-issues.md) | GET |  |

### Envelope

| Action | Method | Description |
| --- | --- | --- |
| [Delete Document Envelope](actions/delete-document-envelope.md) | DELETE |  |
| [List Document Envelopes](actions/list-document-envelopes.md) | GET |  |

### Field

| Action | Method | Description |
| --- | --- | --- |
| [List All Data for a User](actions/list-all-data-for-a-user.md) | GET |  |

### Form

| Action | Method | Description |
| --- | --- | --- |
| [Copy a Form](actions/copy-a-form.md) | POST |  |
| [Create a Form](actions/create-a-form.md) | POST |  |
| [Delete a Form](actions/delete-a-form.md) | DELETE |  |
| [List Forms](actions/list-forms.md) | GET |  |
| [Retrieve Form Schema](actions/retrieve-form-schema.md) | GET |  |
| [Update a Form](actions/update-a-form.md) | PUT |  |

### Hidden Field

| Action | Method | Description |
| --- | --- | --- |
| [Create Hidden Field](actions/create-hidden-field.md) | POST |  |
| [List Hidden Fields](actions/list-hidden-fields.md) | GET |  |

### Log

| Action | Method | Description |
| --- | --- | --- |
| [List API Connector Errors](actions/list-api-connector-errors.md) | GET |  |
| [List Quik Integration Requests](actions/list-quik-integration-requests.md) | GET |  |

### Submission

| Action | Method | Description |
| --- | --- | --- |
| [Create or Update Form Submissions](actions/create-or-update-form-submissions.md) | POST |  |
| [Export Form Submission PDF](actions/export-form-submission-pdf.md) | POST |  |
| [List Form Submissions](actions/list-form-submissions.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create and Fetch a User](actions/create-and-fetch-a-user.md) | POST |  |
| [Delete a User](actions/delete-a-user.md) | DELETE |  |
| [Get User Form Session](actions/get-user-form-session.md) | GET |  |
| [List All Users](actions/list-all-users.md) | GET |  |

