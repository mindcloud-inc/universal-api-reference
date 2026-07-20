# <img src="https://images.mindcloud.co/apps/icons/global-patron_1776776865629.png" alt="Global Patron logo" width="28" height="28"> Global Patron: Universal API

Manage Global Patron forms, submissions, datalists, users, and webhooks through the documented GlobalPatron API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/globalPatron/latest
- **Category:** Marketing
- **Actions:** 36
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.globalpatron.com
- **Vendor API docs:** https://www.globalpatron.com/developers/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Accessible Forms](actions/list-accessible-forms.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/list-accessible-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (36)

### Datalist Entries

| Action | Method | Description |
| --- | --- | --- |
| [Create Datalist Entry Items](actions/create-datalist-entry-items.md) | POST | Adds datalist entry items to Global Patron. |
| [Delete Datalist Entry Item](actions/delete-datalist-entry-item.md) | DELETE | Deletes a datalist entry item from Global Patron. |
| [List Datalist Entry Items](actions/list-datalist-entry-items.md) | GET | Lists datalist entry items in Global Patron. |

### Datalists

| Action | Method | Description |
| --- | --- | --- |
| [Create Datalist](actions/create-datalist.md) | POST | Creates a datalist in Global Patron. |
| [Delete Datalist](actions/delete-datalist.md) | DELETE | Deletes a datalist from Global Patron. |
| [List Accessible Datalists](actions/list-accessible-datalists.md) | GET | Lists accessible datalists in Global Patron. |
| [Update Datalist](actions/update-datalist.md) | PUT | Updates a datalist in Global Patron. |

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [Clone Form](actions/clone-form.md) | POST | Clones a form in Global Patron. |
| [Delete Form](actions/delete-form.md) | DELETE | Deletes a form from Global Patron. |
| [List Accessible Forms](actions/list-accessible-forms.md) | GET | Lists accessible forms in Global Patron. |
| [Retrieve Form JSON](actions/retrieve-form-json.md) | GET | Retrieves form JSON from Global Patron. |
| [Update Form Calculated Fields Settings](actions/update-form-calculated-fields-settings.md) | PUT | Updates form calculated fields settings in Global Patron. |
| [Update Form Conditional Logic Settings](actions/update-form-conditional-logic-settings.md) | PUT | Updates form conditional logic settings in Global Patron. |
| [Update Form Confirmation Email Settings](actions/update-form-confirmation-email-settings.md) | PUT | Updates form confirmation email settings in Global Patron. |
| [Update Form Data Destination Settings](actions/update-form-data-destination-settings.md) | PUT | Updates form data destination settings in Global Patron. |
| [Update Form Dynamic Droplist Settings](actions/update-form-dynamic-droplist-settings.md) | PUT | Updates form dynamic droplist settings in Global Patron. |
| [Update Form General Settings](actions/update-form-general-settings.md) | PUT | Updates form general settings in Global Patron. |
| [Update Form Payment Settings](actions/update-form-payment-settings.md) | PUT | Updates form payment settings in Global Patron. |
| [Update Form Private Datalist Logic Settings](actions/update-form-private-datalist-logic-settings.md) | PUT | Updates form private datalist logic settings in Global Patron. |
| [Update Form Quantity Limit Settings](actions/update-form-quantity-limit-settings.md) | PUT | Updates form quantity limit settings in Global Patron. |
| [Update Form Security Settings](actions/update-form-security-settings.md) | PUT | Updates form security settings in Global Patron. |
| [Update Form Thanks Page Settings](actions/update-form-thanks-page-settings.md) | PUT | Updates form thanks page settings in Global Patron. |

### Submissions

| Action | Method | Description |
| --- | --- | --- |
| [Create Submission](actions/create-submission.md) | POST | Creates a form submission in Global Patron. |
| [Delete Submission](actions/delete-submission.md) | DELETE | Deletes a form submission from Global Patron. |
| [List Form Submissions](actions/list-form-submissions.md) | GET | Lists form submissions in Global Patron. |
| [Retrieve Submission](actions/retrieve-submission.md) | GET | Retrieves a form submission from Global Patron. |
| [Retrieve Submission Attachment](actions/retrieve-submission-attachment.md) | GET | Retrieves a submission attachment download link from Global Patron. |
| [Update Submission](actions/update-submission.md) | PUT | Updates a form submission in Global Patron. |
| [Upload Submission Attachment](actions/upload-submission-attachment.md) | POST | Uploads a submission attachment to Global Patron. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Add Form User](actions/add-form-user.md) | POST | Adds a form user in Global Patron. |
| [Delete Form User](actions/delete-form-user.md) | DELETE | Deletes a form user from Global Patron. |
| [List Form User Security Settings](actions/list-form-user-security-settings.md) | GET | Lists form user security settings in Global Patron. |
| [Update Form User Security Settings](actions/update-form-user-security-settings.md) | PUT | Updates form user security settings in Global Patron. |

### Webhooks

| Action | Method | Description |
| --- | --- | --- |
| [Add Form Submission Webhook](actions/add-form-submission-webhook.md) | POST | Adds a form submission webhook in Global Patron. |
| [Delete Form Submission Webhook](actions/delete-form-submission-webhook.md) | DELETE | Deletes a form submission webhook from Global Patron. |
| [List Form Submission Webhooks](actions/list-form-submission-webhooks.md) | GET | Lists form submission webhooks in Global Patron. |

