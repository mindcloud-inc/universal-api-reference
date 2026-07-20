# <img src="https://images.mindcloud.co/apps/icons/recommand-icon_1776085763374.png" alt="Recommand logo" width="28" height="28"> Recommand: Universal API

Recommand API integration for managing Peppol companies, documents, recipients, webhooks, playgrounds, suppliers, customers, and labels.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/recommand/latest
- **Category:** Commerce / Procurement
- **Actions:** 57
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://recommand.eu
- **Vendor API docs:** https://recommand.eu/en/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Verify Authentication](actions/verify-authentication.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recommand/latest/actions/verify-authentication?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (57)

### Authentication

| Action | Method | Description |
| --- | --- | --- |
| [Verify Authentication](actions/verify-authentication.md) | GET | Validates the current Recommand API credentials. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | POST | Creates a new company in Recommand. |
| [Delete Company](actions/delete-company.md) | DELETE | Deletes an existing company from Recommand. |
| [Get Company](actions/get-company.md) | GET | Retrieves a company record from Recommand. |
| [List Companies](actions/list-companies.md) | GET | Retrieves company records from the Recommand API. |
| [Update Company](actions/update-company.md) | PUT | Updates an existing company in Recommand. |
| [Verify Company](actions/verify-company.md) | GET | Verifies a company profile in Recommand. |

### Company Document Type

| Action | Method | Description |
| --- | --- | --- |
| [Create Company Document Type](actions/create-company-document-type.md) | POST | Creates a new company document type in Recommand. |
| [Delete Company Document Type](actions/delete-company-document-type.md) | DELETE | Deletes a company document type from Recommand. |
| [Get Company Document Type](actions/get-company-document-type.md) | GET | Retrieves a company document type from Recommand. |
| [List Company Document Types](actions/list-company-document-types.md) | GET | Retrieves company document types from Recommand. |
| [Update Company Document Type](actions/update-company-document-type.md) | PUT | Updates an existing company document type in Recommand. |

### Company Identifier

| Action | Method | Description |
| --- | --- | --- |
| [Create Company Identifier](actions/create-company-identifier.md) | POST | Creates a new company identifier in Recommand. |
| [Delete Company Identifier](actions/delete-company-identifier.md) | DELETE | Deletes a company identifier from Recommand. |
| [Get Company Identifier](actions/get-company-identifier.md) | GET | Retrieves a company identifier from Recommand. |
| [List Company Identifiers](actions/list-company-identifiers.md) | GET | Retrieves company identifier records from Recommand. |
| [Update Company Identifier](actions/update-company-identifier.md) | PUT | Updates an existing company identifier in Recommand. |

### Company Notification Email Addresse

| Action | Method | Description |
| --- | --- | --- |
| [Create Company Notification Email Address](actions/create-company-notification-email-address.md) | POST | Creates a company notification email address in Recommand. |
| [Delete Company Notification Email Address](actions/delete-company-notification-email-address.md) | DELETE | Deletes a company notification email address from Recommand. |
| [Get Company Notification Email Address](actions/get-company-notification-email-address.md) | GET | Retrieves a company notification email address from Recommand. |
| [List Company Notification Email Addresses](actions/list-company-notification-email-addresses.md) | GET | Retrieves company notification email addresses from Recommand. |
| [Update Company Notification Email Address](actions/update-company-notification-email-address.md) | PUT | Updates a company notification email address in Recommand. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Delete Customer](actions/delete-customer.md) | DELETE | Deletes an existing customer from Recommand. |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer record from Recommand. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customer records from the Recommand API. |
| [Upsert Customer](actions/upsert-customer.md) | POST | Finds a customer in Recommand, or creates one if no match is found. |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Assign Label to Document](actions/assign-label-to-document.md) | PUT | Assigns a label to a Recommand document. |
| [Delete Document](actions/delete-document.md) | DELETE | Deletes an existing document from Recommand. |
| [Download Document Package](actions/download-document-package.md) | GET | Downloads a document package from Recommand. |
| [Get Document](actions/get-document.md) | GET | Retrieves a document record from Recommand. |
| [Inbox](actions/inbox.md) | GET | Retrieves documents from the Recommand inbox. |
| [List Documents](actions/list-documents.md) | GET | Retrieves document records from the Recommand API. |
| [Mark Document as Read](actions/mark-document-as-read.md) | PUT | Updates a Recommand document as read. |
| [Render Document Preview](actions/render-document-preview.md) | GET | Retrieves a rendered preview for a Recommand document. |
| [Unassign Label from Document](actions/unassign-label-from-document.md) | DELETE | Removes a label from a Recommand document. |

### Label

| Action | Method | Description |
| --- | --- | --- |
| [Create Label](actions/create-label.md) | POST | Creates a new label in Recommand. |
| [Delete Label](actions/delete-label.md) | DELETE | Deletes an existing label from Recommand. |
| [Get Label](actions/get-label.md) | GET | Retrieves a label record from Recommand. |
| [List Labels](actions/list-labels.md) | GET | Retrieves label records from the Recommand API. |
| [Update Label](actions/update-label.md) | PUT | Updates an existing label in Recommand. |

### Playground

| Action | Method | Description |
| --- | --- | --- |
| [Create Playground](actions/create-playground.md) | POST | Creates a new playground in Recommand. |
| [Get Playground](actions/get-playground.md) | GET | Retrieves the current playground from Recommand. |

### Recipient

| Action | Method | Description |
| --- | --- | --- |
| [Search Directory](actions/search-directory.md) | GET | Finds recipients in the Recommand directory. |
| [Verify Document Support](actions/verify-document-support.md) | GET | Verifies document support for a Recommand recipient. |
| [Verify Recipient](actions/verify-recipient.md) | GET | Verifies a recipient in the Recommand directory. |

### Sending

| Action | Method | Description |
| --- | --- | --- |
| [Send Document](actions/send-document.md) | POST | Sends a document through the Recommand network. |

### Supplier

| Action | Method | Description |
| --- | --- | --- |
| [Assign Label to Supplier](actions/assign-label-to-supplier.md) | PUT | Assigns a label to a Recommand supplier. |
| [Delete Supplier](actions/delete-supplier.md) | DELETE | Deletes an existing supplier from Recommand. |
| [Get Supplier](actions/get-supplier.md) | GET | Retrieves a supplier record from Recommand. |
| [List Suppliers](actions/list-suppliers.md) | GET | Retrieves supplier records from the Recommand API. |
| [Unassign Label from Supplier](actions/unassign-label-from-supplier.md) | DELETE | Removes a label from a Recommand supplier. |
| [Upsert Supplier](actions/upsert-supplier.md) | POST | Finds a supplier in Recommand, or creates one if no match is found. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Recommand. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from Recommand. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a webhook record from Recommand. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhook records from the Recommand API. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in Recommand. |

