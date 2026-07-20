# Global Patron: Native API Reference

A consolidated summary of Global Patron's API configuration and 36 documented operations, with links to official documentation.

- **Official docs:** https://www.globalpatron.com/developers/api/
- **API base URL:** `https://api.globalpatron.com`

## Authentication

### GlobalPatron API token

Authenticate with the TokenSecret as the API key and the TokenId as a companion credential header.

### Credentials

- **API Key:** `apiKey` · required
- **Token ID:** `tokenId` · required · GlobalPatron TokenId header value paired with the TokenSecret.

Send these headers with each API request:

```http
TokenId: <tokenId>
TokenSecret: <apiKey>
```

[Official authentication documentation](https://www.globalpatron.com/developers/api/)

## API conventions

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 25). Use `offset` in the query string as the record offset; numbering starts at 0.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (36 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Form Submission Webhook](actions/add-form-submission-webhook.md) | `POST /api/restricted/form/{formId}/submissionwebhook` | [docs](https://www.globalpatron.com/developers/api/webhooks/) |
| [Add Form User](actions/add-form-user.md) | `POST /api/restricted/form/{formId}/usersecurity` | [docs](https://www.globalpatron.com/developers/api/users/) |
| [Clone Form](actions/clone-form.md) | `POST /api/restricted/form/{formId}/clone` | [docs](https://www.globalpatron.com/developers/api/forms/) |
| [Create Datalist](actions/create-datalist.md) | `POST /api/restricted/datalist` | [docs](https://www.globalpatron.com/developers/api/datalists/) |
| [Create Datalist Entry Items](actions/create-datalist-entry-items.md) | `POST /api/restricted/datalist/{datalistId}/entry` | [docs](https://www.globalpatron.com/developers/api/datalists/) |
| [Create Submission](actions/create-submission.md) | `POST /api/form/{formId}/submission` | [docs](https://www.globalpatron.com/developers/api/submissions/) |
| [Delete Datalist](actions/delete-datalist.md) | `POST /api/restricted/datalist/{datalistId}?for_deletion=1` | [docs](https://www.globalpatron.com/developers/api/datalists/) |
| [Delete Datalist Entry Item](actions/delete-datalist-entry-item.md) | `DELETE /api/restricted/datalist/{datalistId}/entry/{datalistEntryId}` | [docs](https://www.globalpatron.com/developers/api/datalists/) |
| [Delete Form](actions/delete-form.md) | `POST /api/restricted/form/{formId}/?updateSettingsOnly=1&settingsSection=generalsettingsdelete` | [docs](https://www.globalpatron.com/developers/api/forms/) |
| [Delete Form Submission Webhook](actions/delete-form-submission-webhook.md) | `DELETE /api/restricted/form/{formId}/submissionwebhook/{submissionWebhookId}` | [docs](https://www.globalpatron.com/developers/api/webhooks/) |
| [Delete Form User](actions/delete-form-user.md) | `DELETE /api/restricted/form/{formId}/usersecurity/{userSecurityDocumentId}` | [docs](https://www.globalpatron.com/developers/api/users/) |
| [Delete Submission](actions/delete-submission.md) | `DELETE /api/restricted/form/{formId}/submission/{submissionId}` | [docs](https://www.globalpatron.com/developers/api/submissions/) |
| [List Accessible Datalists](actions/list-accessible-datalists.md) | `GET /api/restricted/user/datalist` | [docs](https://www.globalpatron.com/developers/api/datalists/) |
| [List Accessible Forms](actions/list-accessible-forms.md) | `GET /api/restricted/user/form` | [docs](https://www.globalpatron.com/developers/api/forms/) |
| [List Datalist Entry Items](actions/list-datalist-entry-items.md) | `GET /api/restricted/datalist/{datalistId}/entries` | [docs](https://www.globalpatron.com/developers/api/datalists/) |
| [List Form Submission Webhooks](actions/list-form-submission-webhooks.md) | `GET /api/restricted/form/{formId}/submissionwebhook` | [docs](https://www.globalpatron.com/developers/api/webhooks/) |
| [List Form Submissions](actions/list-form-submissions.md) | `GET /api/restricted/form/{formId}/submissions` | [docs](https://www.globalpatron.com/developers/api/submissions/) |
| [List Form User Security Settings](actions/list-form-user-security-settings.md) | `GET /api/restricted/form/{formId}/usersecurity` | [docs](https://www.globalpatron.com/developers/api/users/) |
| [Retrieve Form JSON](actions/retrieve-form-json.md) | `GET /api/form/{formId}` | [docs](https://www.globalpatron.com/developers/api/forms/) |
| [Retrieve Submission](actions/retrieve-submission.md) | `GET /api/restricted/form/{formId}/submission/{submissionId}` | [docs](https://www.globalpatron.com/developers/api/submissions/) |
| [Retrieve Submission Attachment](actions/retrieve-submission-attachment.md) | `GET /api/restricted/form/{formId}/submissionattachment/{attachmentId}` | [docs](https://www.globalpatron.com/developers/api/submissions/) |
| [Update Datalist](actions/update-datalist.md) | `POST /api/restricted/datalist/{datalistId}` | [docs](https://www.globalpatron.com/developers/api/datalists/) |
| [Update Form Calculated Fields Settings](actions/update-form-calculated-fields-settings.md) | `POST /api/restricted/form/{formId}/?updateSettingsOnly=1&settingsSection=calculatedfieldsettings` | [docs](https://www.globalpatron.com/developers/api/forms/) |
| [Update Form Conditional Logic Settings](actions/update-form-conditional-logic-settings.md) | `POST /api/restricted/form/{formId}/?updateSettingsOnly=1&settingsSection=conditionallogicsettings` | [docs](https://www.globalpatron.com/developers/api/forms/) |
| [Update Form Confirmation Email Settings](actions/update-form-confirmation-email-settings.md) | `POST /api/restricted/form/{formId}/?updateSettingsOnly=1&settingsSection=confirmationemailsettings` | [docs](https://www.globalpatron.com/developers/api/forms/) |
| [Update Form Data Destination Settings](actions/update-form-data-destination-settings.md) | `POST /api/restricted/form/{formId}/?updateSettingsOnly=1&settingsSection=destinationsettings` | [docs](https://www.globalpatron.com/developers/api/forms/) |
| [Update Form Dynamic Droplist Settings](actions/update-form-dynamic-droplist-settings.md) | `POST /api/restricted/form/{formId}/?updateSettingsOnly=1&settingsSection=dynamicdatafieldsettings` | [docs](https://www.globalpatron.com/developers/api/forms/) |
| [Update Form General Settings](actions/update-form-general-settings.md) | `POST /api/restricted/form/{formId}/?updateSettingsOnly=1&settingsSection=generalsettings` | [docs](https://www.globalpatron.com/developers/api/forms/) |
| [Update Form Payment Settings](actions/update-form-payment-settings.md) | `POST /api/restricted/form/{formId}/?updateSettingsOnly=1&settingsSection=paymentsettings` | [docs](https://www.globalpatron.com/developers/api/forms/) |
| [Update Form Private Datalist Logic Settings](actions/update-form-private-datalist-logic-settings.md) | `POST /api/restricted/form/{formId}/?updateSettingsOnly=1&settingsSection=privatedatalistlogicsettings` | [docs](https://www.globalpatron.com/developers/api/forms/) |
| [Update Form Quantity Limit Settings](actions/update-form-quantity-limit-settings.md) | `POST /api/restricted/form/{formId}/?updateSettingsOnly=1&settingsSection=quantitylimitsettings` | [docs](https://www.globalpatron.com/developers/api/forms/) |
| [Update Form Security Settings](actions/update-form-security-settings.md) | `POST /api/restricted/form/{formId}/?updateSettingsOnly=1&settingsSection=securitysettings` | [docs](https://www.globalpatron.com/developers/api/forms/) |
| [Update Form Thanks Page Settings](actions/update-form-thanks-page-settings.md) | `POST /api/restricted/form/{formId}/?updateSettingsOnly=1&settingsSection=thankspagesettings` | [docs](https://www.globalpatron.com/developers/api/forms/) |
| [Update Form User Security Settings](actions/update-form-user-security-settings.md) | `POST /api/restricted/form/{formId}/usersecurity/{userSecurityId}` | [docs](https://www.globalpatron.com/developers/api/users/) |
| [Update Submission](actions/update-submission.md) | `POST /api/restricted/form/{formId}/submission/{submissionId}` | [docs](https://www.globalpatron.com/developers/api/submissions/) |
| [Upload Submission Attachment](actions/upload-submission-attachment.md) | `POST /api/form/{formId}/submissionattachment` | [docs](https://www.globalpatron.com/developers/api/submissions/) |
