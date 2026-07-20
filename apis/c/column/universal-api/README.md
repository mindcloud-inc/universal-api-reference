# <img src="https://images.mindcloud.co/apps/icons/column_1776979389542.png" alt="Column logo" width="28" height="28"> Column: Universal API

Open accounts, move money, and manage entities and transfers

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/column/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://column.com
- **Vendor API docs:** https://column.com/docs/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Financial Institutions](actions/list-financial-institutions.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/column/latest/actions/list-financial-institutions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Account Number

| Action | Method | Description |
| --- | --- | --- |
| [Create Account Number](actions/create-account-number.md) | POST |  |
| [List Account Numbers](actions/list-account-numbers.md) | GET |  |

### Ach Transfer

| Action | Method | Description |
| --- | --- | --- |
| [Cancel ACH Transfer](actions/cancel-ach-transfer.md) | PUT |  |
| [Create ACH Transfer](actions/create-ach-transfer.md) | POST |  |
| [Get ACH Transfer](actions/get-ach-transfer.md) | GET |  |
| [List ACH Transfers](actions/list-ach-transfers.md) | GET |  |

### Ach Transfer Reversal

| Action | Method | Description |
| --- | --- | --- |
| [Reverse ACH Transfer](actions/reverse-ach-transfer.md) | POST |  |

### Additional Requirements

| Action | Method | Description |
| --- | --- | --- |
| [Get Additional Requirements](actions/get-additional-requirements.md) | GET |  |
| [Submit Additional Requirements](actions/submit-additional-requirements.md) | PUT |  |

### Associated Person

| Action | Method | Description |
| --- | --- | --- |
| [Link Associated Person](actions/link-associated-person.md) | POST |  |
| [List Associated Persons](actions/list-associated-persons.md) | GET |  |

### Bank Account

| Action | Method | Description |
| --- | --- | --- |
| [Create Bank Account](actions/create-bank-account.md) | POST |  |
| [Get Bank Account](actions/get-bank-account.md) | GET |  |
| [List Bank Accounts](actions/list-bank-accounts.md) | GET |  |
| [Update Bank Account](actions/update-bank-account.md) | PUT |  |

### Book Transfer

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Book Transfer](actions/cancel-book-transfer.md) | PUT |  |
| [Create Book Transfer](actions/create-book-transfer.md) | POST |  |
| [Get Book Transfer](actions/get-book-transfer.md) | GET |  |
| [List Book Transfers](actions/list-book-transfers.md) | GET |  |

### Business Entity

| Action | Method | Description |
| --- | --- | --- |
| [Create Business Entity](actions/create-business-entity.md) | POST |  |
| [Update Business Entity](actions/update-business-entity.md) | PUT |  |

### Counterparty

| Action | Method | Description |
| --- | --- | --- |
| [Create Counterparty](actions/create-counterparty.md) | POST |  |
| [Get Counterparty](actions/get-counterparty.md) | GET |  |
| [List Counterparties](actions/list-counterparties.md) | GET |  |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Get Document](actions/get-document.md) | GET |  |
| [List Documents](actions/list-documents.md) | GET |  |
| [Upload Document](actions/upload-document.md) | POST |  |

### Entity

| Action | Method | Description |
| --- | --- | --- |
| [Get Entity](actions/get-entity.md) | GET |  |
| [List Entities](actions/list-entities.md) | GET |  |

### Entity Compliance

| Action | Method | Description |
| --- | --- | --- |
| [Get Entity Compliance](actions/get-entity-compliance.md) | GET |  |

### Evidence

| Action | Method | Description |
| --- | --- | --- |
| [Create Evidence With File Upload](actions/create-evidence-with-file-upload.md) | POST |  |
| [List Entity Evidence](actions/list-entity-evidence.md) | GET |  |

### Financial Institution

| Action | Method | Description |
| --- | --- | --- |
| [Get Financial Institution](actions/get-financial-institution.md) | GET |  |
| [List Financial Institutions](actions/list-financial-institutions.md) | GET |  |

### Person Entity

| Action | Method | Description |
| --- | --- | --- |
| [Create Person Entity](actions/create-person-entity.md) | POST |  |
| [Update Person Entity](actions/update-person-entity.md) | PUT |  |

### Transfer

| Action | Method | Description |
| --- | --- | --- |
| [List All Transfers](actions/list-all-transfers.md) | GET |  |

### Wire Transfer

| Action | Method | Description |
| --- | --- | --- |
| [Create Wire Transfer](actions/create-wire-transfer.md) | POST |  |
| [Get Wire Transfer](actions/get-wire-transfer.md) | GET |  |
| [List Wire Transfers](actions/list-wire-transfers.md) | GET |  |

