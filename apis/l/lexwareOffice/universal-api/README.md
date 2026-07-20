# <img src="https://images.mindcloud.co/apps/icons/lexware-office_1773327629072.png" alt="Lexware Office logo" width="28" height="28"> Lexware Office: Universal API

Create invoices, manage bookkeeping, banking, payroll, and taxes

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/lexwareOffice/latest
- **Category:** Commerce / Accounting
- **Actions:** 34
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://office.lexware.de/
- **Vendor API docs:** https://developers.lexware.io/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Retrieve Profile Information](actions/retrieve-profile-information.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/retrieve-profile-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (34)

### Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Upload File](actions/upload-file.md) | POST | Uploads a bookkeeping voucher file to Lexware Office. |
| [Upload File to Voucher](actions/upload-file-to-voucher.md) | POST | Uploads a file to a voucher in Lexware Office. |

### Company Info

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Profile Information](actions/retrieve-profile-information.md) | GET | Retrieves profile information from Lexware Office. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Lexware Office. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves a list of contacts from Lexware Office. |
| [Retrieve Contact](actions/retrieve-contact.md) | GET | Retrieves a contact from Lexware Office. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Lexware Office. |

### Credit Note Document

| Action | Method | Description |
| --- | --- | --- |
| [Render Credit Note Document](actions/render-credit-note-document.md) | GET | Retrieves a rendered credit note PDF from Lexware Office. |

### Credit Note File

| Action | Method | Description |
| --- | --- | --- |
| [Download Credit Note File](actions/download-credit-note-file.md) | GET | Downloads a credit note file from Lexware Office. |

### Credit Notes

| Action | Method | Description |
| --- | --- | --- |
| [Create Credit Note](actions/create-credit-note.md) | POST | Creates a new credit note in Lexware Office. |
| [Retrieve Credit Note](actions/retrieve-credit-note.md) | GET | Retrieves a credit note from Lexware Office. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Download File](actions/download-file.md) | GET | Downloads a bookkeeping voucher file from Lexware Office. |

### Invoice Document

| Action | Method | Description |
| --- | --- | --- |
| [Render Invoice Document](actions/render-invoice-document.md) | GET | Retrieves a rendered invoice PDF from Lexware Office. |

### Invoice File

| Action | Method | Description |
| --- | --- | --- |
| [Download Invoice File](actions/download-invoice-file.md) | GET | Downloads an invoice file from Lexware Office. |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Create Invoice](actions/create-invoice.md) | POST | Creates a new invoice in Lexware Office. |
| [Retrieve Invoice](actions/retrieve-invoice.md) | GET | Retrieves an invoice from Lexware Office. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Create Article](actions/create-article.md) | POST | Creates a new article in Lexware Office. |
| [Delete Article](actions/delete-article.md) | DELETE | Deletes an existing article from Lexware Office. |
| [List Articles](actions/list-articles.md) | GET | Retrieves a list of articles from Lexware Office. |
| [Retrieve Article](actions/retrieve-article.md) | GET | Retrieves an article from Lexware Office. |
| [Update Article](actions/update-article.md) | PUT | Updates an existing article in Lexware Office. |

### Order Confirmation

| Action | Method | Description |
| --- | --- | --- |
| [Create Order Confirmation](actions/create-order-confirmation.md) | POST | Creates a new order confirmation in Lexware Office. |
| [Retrieve Order Confirmation](actions/retrieve-order-confirmation.md) | GET | Retrieves an order confirmation from Lexware Office. |

### Order Confirmation Document

| Action | Method | Description |
| --- | --- | --- |
| [Render Order Confirmation Document](actions/render-order-confirmation-document.md) | GET | Retrieves a rendered order confirmation PDF from Lexware Office. |

### Order Confirmation File

| Action | Method | Description |
| --- | --- | --- |
| [Download Order Confirmation File](actions/download-order-confirmation-file.md) | GET | Downloads an order confirmation file from Lexware Office. |

### Payment

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Voucher Payments](actions/retrieve-voucher-payments.md) | GET | Retrieves payment information for a voucher in Lexware Office. |

### Quotation

| Action | Method | Description |
| --- | --- | --- |
| [Create Quotation](actions/create-quotation.md) | POST | Creates a new quotation in Lexware Office. |
| [Retrieve Quotation](actions/retrieve-quotation.md) | GET | Retrieves a quotation from Lexware Office. |

### Quotation Document

| Action | Method | Description |
| --- | --- | --- |
| [Render Quotation Document](actions/render-quotation-document.md) | GET | Retrieves a rendered quotation PDF from Lexware Office. |

### Quotation File

| Action | Method | Description |
| --- | --- | --- |
| [Download Quotation File](actions/download-quotation-file.md) | GET | Downloads a quotation file from Lexware Office. |

### Voucher

| Action | Method | Description |
| --- | --- | --- |
| [Create Voucher](actions/create-voucher.md) | POST | Creates a new voucher in Lexware Office. |
| [List Voucher Metadata](actions/list-voucher-metadata.md) | GET | Retrieves and filters voucher metadata in Lexware Office. |
| [Retrieve Voucher](actions/retrieve-voucher.md) | GET | Retrieves a voucher from Lexware Office. |
| [Update Voucher](actions/update-voucher.md) | PUT | Updates an existing voucher in Lexware Office. |

