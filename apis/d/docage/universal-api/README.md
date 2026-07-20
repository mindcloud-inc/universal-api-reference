# <img src="https://images.mindcloud.co/apps/icons/docage_1774898333420.png" alt="Docage logo" width="28" height="28"> Docage: Universal API

Docage is a document workflow and e-signature platform for managing organizations, boxes, contacts, documents, and transactions.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/docage/latest
- **Category:** Productivity / Legal & Contracts
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.docage.com/
- **Vendor API docs:** https://documentation.docage.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Organizations](actions/list-organizations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docage/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Docage. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from Docage. |
| [Get Contact By Email](actions/get-contact-by-email.md) | GET | Retrieves a contact from Docage by email. |
| [Get Contact By ID](actions/get-contact-by-id.md) | GET | Retrieves a contact from Docage by ID. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves accessible contacts from Docage. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Docage. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Create Document](actions/create-document.md) | POST | Creates a new document in Docage. |
| [Delete Document](actions/delete-document.md) | DELETE | Deletes an existing document from Docage. |
| [Get Document By ID](actions/get-document-by-id.md) | GET | Retrieves a document from Docage by ID. |
| [List Documents](actions/list-documents.md) | GET | Retrieves accessible documents from Docage. |
| [Update Document](actions/update-document.md) | PUT | Updates an existing document in Docage. |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [Create Box](actions/create-box.md) | POST | Creates a new box in Docage. |
| [Delete Box](actions/delete-box.md) | DELETE | Deletes an existing box from Docage. |
| [Get Box By ID](actions/get-box-by-id.md) | GET | Retrieves a box from Docage by ID. |
| [Get Box By Name](actions/get-box-by-name.md) | GET | Retrieves a box from Docage by name. |
| [List Boxes](actions/list-boxes.md) | GET | Retrieves accessible boxes from Docage. |
| [Update Box](actions/update-box.md) | PUT | Updates an existing box in Docage. |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves accessible organizations from Docage. |

### Transactions

| Action | Method | Description |
| --- | --- | --- |
| [Create Transaction](actions/create-transaction.md) | POST | Creates a new transaction in Docage. |
| [Delete Transaction](actions/delete-transaction.md) | DELETE | Deletes an existing transaction from Docage. |
| [Get Transaction By ID](actions/get-transaction-by-id.md) | GET | Retrieves a transaction from Docage by ID. |
| [Get Transaction Status](actions/get-transaction-status.md) | GET | Retrieves the status of a Docage transaction. |
| [Launch Transaction](actions/launch-transaction.md) | PUT | Launches a transaction in Docage. |
| [List Transaction Documents](actions/list-transaction-documents.md) | GET | Downloads all documents from a Docage transaction. |
| [List Transaction Members](actions/list-transaction-members.md) | GET | Retrieves the members of a Docage transaction. |
| [List Transactions](actions/list-transactions.md) | GET | Retrieves accessible transactions from Docage. |
| [Update Transaction](actions/update-transaction.md) | PUT | Updates an existing transaction in Docage. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Docage User By Email](actions/get-docage-user-by-email.md) | GET | Retrieves a user from Docage by email. |
| [Get Docage User By ID](actions/get-docage-user-by-id.md) | GET | Retrieves a user from Docage by ID. |
| [List Docage Users](actions/list-docage-users.md) | GET | Retrieves accessible users from Docage. |

