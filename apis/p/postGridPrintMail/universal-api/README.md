# <img src="https://images.mindcloud.co/apps/icons/post-grid-print-mail_1773930822984.png" alt="PostGrid Print & Mail logo" width="28" height="28"> PostGrid Print & Mail: Universal API

Create, send, and track direct mail, templates, and contacts

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/postGridPrintMail/latest
- **Category:** Marketing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.postgrid.com/
- **Vendor API docs:** https://docs.postgrid.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Contacts](actions/list-contacts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postGridPrintMail/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Bank Account

| Action | Method | Description |
| --- | --- | --- |
| [Create Bank Account](actions/create-bank-account.md) | POST | Creates a bank account in PostGrid Print & Mail. |
| [Get Bank Account](actions/get-bank-account.md) | GET | Retrieves a bank account from PostGrid Print & Mail. |
| [List Bank Accounts](actions/list-bank-accounts.md) | GET | Retrieves bank accounts from PostGrid Print & Mail. |

### Cheque

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Cheque](actions/cancel-cheque.md) | DELETE | Cancels a cheque in PostGrid Print & Mail. |
| [Create Cheque](actions/create-cheque.md) | POST | Creates a cheque in PostGrid Print & Mail. |
| [Get Cheque](actions/get-cheque.md) | GET | Retrieves a cheque from PostGrid Print & Mail. |
| [List Cheques](actions/list-cheques.md) | GET | Retrieves cheques from PostGrid Print & Mail. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a contact in PostGrid Print & Mail. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes a contact from PostGrid Print & Mail. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from PostGrid Print & Mail. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from PostGrid Print & Mail. |

### Letter

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Letter](actions/cancel-letter.md) | DELETE | Cancels a letter in PostGrid Print & Mail. |
| [Create Letter](actions/create-letter.md) | POST | Creates a letter in PostGrid Print & Mail. |
| [Get Letter](actions/get-letter.md) | GET | Retrieves a letter from PostGrid Print & Mail. |
| [List Letters](actions/list-letters.md) | GET | Retrieves letters from PostGrid Print & Mail. |

### Postcard

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Postcard](actions/cancel-postcard.md) | DELETE | Cancels a postcard in PostGrid Print & Mail. |
| [Create Postcard](actions/create-postcard.md) | POST | Creates a postcard in PostGrid Print & Mail. |
| [Get Postcard](actions/get-postcard.md) | GET | Retrieves a postcard from PostGrid Print & Mail. |
| [List Postcards](actions/list-postcards.md) | GET | Retrieves postcards from PostGrid Print & Mail. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Create Template](actions/create-template.md) | POST | Creates a template in PostGrid Print & Mail. |
| [Delete Template](actions/delete-template.md) | DELETE | Deletes a template from PostGrid Print & Mail. |
| [Get Template](actions/get-template.md) | GET | Retrieves a template from PostGrid Print & Mail. |
| [List Templates](actions/list-templates.md) | GET | Retrieves templates from PostGrid Print & Mail. |
| [Update Template](actions/update-template.md) | PUT | Updates a template in PostGrid Print & Mail. |

