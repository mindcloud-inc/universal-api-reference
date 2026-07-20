# Docage: Native API Reference

A consolidated summary of Docage's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://documentation.docage.com/
- **OpenAPI specification:** https://api.docage.com/swagger/v1/swagger.json
- **API base URL:** `https://api.docage.com`

## Authentication

### Basic

Use your Docage login email as the username and your generated Docage API key as the password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://docapiv2.docage.com/)

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Box](actions/create-box.md) | `POST /Boxes` | [docs](https://documentation.docage.com/cr%C3%A9er-un-classeur-23280582e0) |
| [Create Contact](actions/create-contact.md) | `POST /Contacts` | [docs](https://documentation.docage.com/cr%C3%A9er-un-contact-23707615e0) |
| [Create Document](actions/create-document.md) | `POST /Documents` | [docs](https://documentation.docage.com/cr%C3%A9er-un-document-23707655e0) |
| [Create Transaction](actions/create-transaction.md) | `POST /Transactions` | [docs](https://documentation.docage.com/cr%C3%A9er-un-parcours-seul-23707899e0) |
| [Delete Box](actions/delete-box.md) | `DELETE /Boxes/:id` | [docs](https://documentation.docage.com/supprimer-un-classeur-23707564e0) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /Contacts/:id` | [docs](https://documentation.docage.com/supprimer-un-contact-23707611e0) |
| [Delete Document](actions/delete-document.md) | `DELETE /Documents/:id` | [docs](https://documentation.docage.com/suppression-dun-document-23707651e0) |
| [Delete Transaction](actions/delete-transaction.md) | `DELETE /Transactions/:id` | [docs](https://documentation.docage.com/supprimer-un-parcours-23707882e0) |
| [Get Box By ID](actions/get-box-by-id.md) | `GET /Boxes/ById/:id` | [docs](https://documentation.docage.com/obtenir-un-classeur-par-son-id-23707576e0) |
| [Get Box By Name](actions/get-box-by-name.md) | `GET /Boxes/ByName/:name` | [docs](https://documentation.docage.com/obtenir-un-classeur-par-son-nom-23707566e0) |
| [Get Contact By Email](actions/get-contact-by-email.md) | `GET /Contacts/byemail/:email` | [docs](https://documentation.docage.com/obtenir-un-contact-par-son-email-23707613e0) |
| [Get Contact By ID](actions/get-contact-by-id.md) | `GET /Contacts/ById/:id` | [docs](https://documentation.docage.com/obtenir-un-contact-par-son-id-23707622e0) |
| [Get Docage User By Email](actions/get-docage-user-by-email.md) | `GET /DocageUsers/byemail/:email` | [docs](https://documentation.docage.com/obtenir-un-utilisateur-par-son-email-23707629e0) |
| [Get Docage User By ID](actions/get-docage-user-by-id.md) | `GET /DocageUsers/ById/:id` | [docs](https://documentation.docage.com/obtenir-un-utilisateur-par-son-id-23707639e0) |
| [Get Document By ID](actions/get-document-by-id.md) | `GET /Documents/ById/:id` | [docs](https://documentation.docage.com/obtenir-un-document-par-son-id-23707662e0) |
| [Get Transaction By ID](actions/get-transaction-by-id.md) | `GET /Transactions/ById/:id` | [docs](https://documentation.docage.com/obtenir-un-parcours-par-son-id-23707906e0) |
| [Get Transaction Status](actions/get-transaction-status.md) | `GET /Transactions/Status/:id` | [docs](https://documentation.docage.com/r%C3%A9cup%C3%A9rer-le-statut-dune-transaction-23280563e0) |
| [Launch Transaction](actions/launch-transaction.md) | `POST /Transactions/LaunchTransaction/:id` | [docs](https://documentation.docage.com/lancer-une-transaction-23280555e0) |
| [List Boxes](actions/list-boxes.md) | `GET /Boxes` | [docs](https://documentation.docage.com/obtenir-tous-les-classeurs-accessibles-par-lutilisateur-23707569e0) |
| [List Contacts](actions/list-contacts.md) | `GET /Contacts` | [docs](https://documentation.docage.com/obtenir-tous-les-contacts-accessibles-par-lutilisateur-23280521e0) |
| [List Docage Users](actions/list-docage-users.md) | `GET /DocageUsers` | [docs](https://documentation.docage.com/obtenir-tous-les-utilisateurs-accessibles-par-lutilisateur-23707632e0) |
| [List Documents](actions/list-documents.md) | `GET /Documents` | [docs](https://documentation.docage.com/obtenir-tous-les-documents-accessibles-par-lutilisateur-23707654e0) |
| [List Organizations](actions/list-organizations.md) | `GET /Organizations` | [docs](https://documentation.docage.com/obtenir-toutes-les-organisations-accessibles-par-lutilisateur-23707774e0) |
| [List Transaction Documents](actions/list-transaction-documents.md) | `GET /Transactions/GetTransactionFiles/:id` | [docs](https://documentation.docage.com/t%C3%A9l%C3%A9charger-tous-les-documents-dune-transaction-23280557e0) |
| [List Transaction Members](actions/list-transaction-members.md) | `GET /Transactions/GetTransactionMembers/:id` | [docs](https://documentation.docage.com/obtenir-les-membres-dun-parcours-23707884e0) |
| [List Transactions](actions/list-transactions.md) | `GET /Transactions` | [docs](https://documentation.docage.com/obtenir-tous-les-parcours-accessibles-par-lutilisateur-23280518e0) |
| [Update Box](actions/update-box.md) | `PUT /Boxes/:id` | [docs](https://documentation.docage.com/modifier-un-classeur-23707565e0) |
| [Update Contact](actions/update-contact.md) | `PUT /Contacts/:id` | [docs](https://documentation.docage.com/modifier-un-contact-23707612e0) |
| [Update Document](actions/update-document.md) | `PUT /Documents/:id` | [docs](https://documentation.docage.com/modifier-un-document-23707652e0) |
| [Update Transaction](actions/update-transaction.md) | `PUT /Transactions/:id` | [docs](https://documentation.docage.com/modifier-un-parcours-23707883e0) |
