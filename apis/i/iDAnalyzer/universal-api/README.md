# <img src="https://images.mindcloud.co/apps/icons/favicon_1777490962575.png" alt="ID Analyzer logo" width="28" height="28"> ID Analyzer: Universal API

Identity verification and KYC platform for document OCR, biometric verification, AML screening, KYC profile management, and transaction retrieval.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/iDAnalyzer/latest
- **Category:** IT Operations / Security & Identity
- **Actions:** 19
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.idanalyzer.com/
- **Vendor API docs:** https://developer.idanalyzer.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List KYC Profiles](actions/list-kyc-profiles.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iDAnalyzer/latest/actions/list-kyc-profiles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (19)

### Document Template

| Action | Method | Description |
| --- | --- | --- |
| [Create a document template](actions/create-a-document-template.md) | POST | Creates a document template in ID Analyzer. |
| [Delete a document template](actions/delete-a-document-template.md) | DELETE | Deletes a document template from ID Analyzer. |
| [Get a document template](actions/get-a-document-template.md) | GET | Retrieves a document template from ID Analyzer. |
| [List document templates](actions/list-document-templates.md) | GET | Retrieves document templates from ID Analyzer. |
| [Update a document template](actions/update-a-document-template.md) | PUT | Updates a document template in ID Analyzer. |

### Docupass Session

| Action | Method | Description |
| --- | --- | --- |
| [Create a hosted Docupass flow](actions/create-a-hosted-docupass-flow.md) | POST | Creates a hosted Docupass flow in ID Analyzer. |
| [Delete a Docupass session](actions/delete-a-docupass-session.md) | DELETE | Deletes a Docupass session from ID Analyzer. |
| [Get a Docupass session](actions/get-a-docupass-session.md) | GET | Retrieves a Docupass session from ID Analyzer. |
| [List Docupass sessions](actions/list-docupass-sessions.md) | GET | Retrieves Docupass sessions from ID Analyzer. |

### Generated Document

| Action | Method | Description |
| --- | --- | --- |
| [Generate a document from a template](actions/generate-a-document-from-a-template.md) | POST | Creates a document from a template in ID Analyzer. |

### Kyc Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get a KYC profile](actions/get-akyc-profile.md) | GET | Retrieves a KYC profile from ID Analyzer. |
| [List KYC Profiles](actions/list-kyc-profiles.md) | GET | Retrieves KYC profiles from ID Analyzer. |

### Ocr Scan Result

| Action | Method | Description |
| --- | --- | --- |
| [Run a fast OCR document scan](actions/run-a-fast-ocr-document-scan.md) | POST | Creates a fast OCR document scan in ID Analyzer. |

### Saved Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Delete a saved transaction](actions/delete-a-saved-transaction.md) | DELETE | Deletes a saved transaction from ID Analyzer. |
| [Get a saved transaction](actions/get-a-saved-transaction.md) | GET | Retrieves a saved transaction from ID Analyzer. |
| [List saved transactions](actions/list-saved-transactions.md) | GET | Retrieves saved transactions from ID Analyzer. |
| [Update the final transaction decision](actions/update-the-final-transaction-decision.md) | PUT | Updates a saved transaction decision in ID Analyzer. |

### Transaction Export

| Action | Method | Description |
| --- | --- | --- |
| [Export saved transactions](actions/export-saved-transactions.md) | POST | Creates a saved transaction export in ID Analyzer. |

### Verification Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Run a full ID verification scan](actions/run-a-full-id-verification-scan.md) | POST | Creates a full ID verification scan in ID Analyzer. |

