# <img src="https://images.mindcloud.co/apps/icons/ugosign_1775657815122.png" alt="Ugosign logo" width="28" height="28"> Ugosign: Universal API

Ugosign: Manage contacts, contracts, envelopes, and signatures

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ugosign/latest
- **Category:** Productivity / Legal & Contracts
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://ugosign.com
- **Vendor API docs:** https://app.ugosign.com/api/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Organization](actions/get-organization.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ugosign/latest/actions/get-organization?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Ugosign. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes a contact from Ugosign. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Ugosign. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Ugosign. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Ugosign. |

### Contract

| Action | Method | Description |
| --- | --- | --- |
| [Create Contract](actions/create-contract.md) | POST | Creates a new contract in Ugosign. |
| [Delete Contract](actions/delete-contract.md) | DELETE | Deletes a contract from Ugosign. |
| [Get Contract](actions/get-contract.md) | GET | Retrieves a contract from Ugosign. |
| [Get Contract Custom Vars](actions/get-contract-custom-vars.md) | GET | Retrieves a contract's custom variables from Ugosign. |
| [List Contracts](actions/list-contracts.md) | GET | Retrieves contracts from Ugosign. |
| [Search Contracts](actions/search-contracts.md) | GET | Finds a contract in Ugosign by ID or text. |
| [Update Contract](actions/update-contract.md) | PUT | Updates an existing contract in Ugosign. |

### Envelope

| Action | Method | Description |
| --- | --- | --- |
| [Create Envelope](actions/create-envelope.md) | POST | Creates a new envelope in Ugosign. |
| [Create Quick Envelope](actions/create-quick-envelope.md) | POST | Creates a contact, contract, and envelope in Ugosign. |
| [Get Envelope](actions/get-envelope.md) | GET | Retrieves an envelope from Ugosign. |
| [List Envelopes](actions/list-envelopes.md) | GET | Retrieves envelopes from Ugosign. |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST | Creates a new folder in Ugosign. |
| [List Folders](actions/list-folders.md) | GET | Retrieves folders from Ugosign. |

### Member

| Action | Method | Description |
| --- | --- | --- |
| [List Members](actions/list-members.md) | GET | Retrieves members from Ugosign. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization](actions/get-organization.md) | GET | Retrieves an organization summary from Ugosign. |

