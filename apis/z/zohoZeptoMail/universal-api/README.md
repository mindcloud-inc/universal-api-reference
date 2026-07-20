# <img src="https://images.mindcloud.co/apps/icons/615b1085-140f-46e1-805d-bc41cc330f52_1775233776866.png" alt="Zoho ZeptoMail logo" width="28" height="28"> Zoho ZeptoMail: Universal API

Send transactional emails, manage templates, domains, suppressions, and email logs

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zohoZeptoMail/latest
- **Category:** Communication / Email Communications
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.zoho.com/zeptomail/
- **Vendor API docs:** https://www.zoho.com/zeptomail/help/api-index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Download Export](actions/download-export.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/download-export?connectionId=$CONNECTION_ID&exportType=string&exportId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Domain

| Action | Method | Description |
| --- | --- | --- |
| [Add Domain](actions/add-domain.md) | POST | Adds a new domain in Zoho ZeptoMail. |
| [Get Domain](actions/get-domain.md) | GET | Retrieves domain details from Zoho ZeptoMail. |
| [List Domains](actions/list-domains.md) | GET | Retrieves domains from Zoho ZeptoMail. |
| [Update Domain](actions/update-domain.md) | PUT | Updates an existing domain in Zoho ZeptoMail. |
| [Verify Domain](actions/verify-domain.md) | PUT | Verifies an existing domain in Zoho ZeptoMail. |

### Emails

| Action | Method | Description |
| --- | --- | --- |
| [Add Template](actions/add-template.md) | POST | Creates a new email template in Zoho ZeptoMail. |
| [Delete Template](actions/delete-template.md) | DELETE | Deletes an email template from Zoho ZeptoMail. |
| [Get Email Log](actions/get-email-log.md) | GET | Retrieves a specific email log from Zoho ZeptoMail. |
| [Get Template](actions/get-template.md) | GET | Retrieves an email template from Zoho ZeptoMail. |
| [List Email Logs](actions/list-email-logs.md) | GET | Retrieves email logs from Zoho ZeptoMail. |
| [List Templates](actions/list-templates.md) | GET | Retrieves email templates from Zoho ZeptoMail. |
| [Send Batch Email](actions/send-batch-email.md) | POST | Sends transactional emails in bulk through Zoho ZeptoMail. |
| [Send Batch Email with Template](actions/send-batch-email-with-template.md) | POST | Sends batch emails from a template in Zoho ZeptoMail. |
| [Send Email](actions/send-email.md) | POST | Sends a transactional email through Zoho ZeptoMail. |
| [Send Email with Template](actions/send-email-with-template.md) | POST | Sends an email from a template in Zoho ZeptoMail. |
| [Update Template](actions/update-template.md) | PUT | Updates an existing email template in Zoho ZeptoMail. |

### Export

| Action | Method | Description |
| --- | --- | --- |
| [Create Export](actions/create-export.md) | POST | Creates a new export for Zoho ZeptoMail logs. |
| [Download Export](actions/download-export.md) | GET | Downloads a log export from Zoho ZeptoMail. |
| [List Exports](actions/list-exports.md) | GET | Retrieves log exports from Zoho ZeptoMail. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Upload File to Cache](actions/upload-file-to-cache.md) | POST | Uploads a file to the Zoho ZeptoMail cache. |

### Suppression

| Action | Method | Description |
| --- | --- | --- |
| [Add Suppression](actions/add-suppression.md) | POST | Adds a suppression list entry in Zoho ZeptoMail. |
| [Delete Suppression](actions/delete-suppression.md) | DELETE | Deletes a suppression list entry from Zoho ZeptoMail. |
| [Edit Suppression](actions/edit-suppression.md) | PUT | Updates a suppression list entry in Zoho ZeptoMail. |
| [List Suppressions](actions/list-suppressions.md) | GET | Retrieves suppression list entries from Zoho ZeptoMail. |

