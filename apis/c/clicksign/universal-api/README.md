# <img src="https://images.mindcloud.co/apps/icons/clicksign_1773847275605.png" alt="Clicksign logo" width="28" height="28"> Clicksign: Universal API

Create envelopes, manage signers, and send documents for signature

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/clicksign/latest
- **Category:** Productivity / Legal & Contracts
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.clicksign.com
- **Vendor API docs:** https://developers.clicksign.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Envelopes](actions/list-envelopes.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clicksign/latest/actions/list-envelopes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Create Document](actions/create-document.md) | POST | Creates a document in a Clicksign envelope. |
| [Delete Document](actions/delete-document.md) | DELETE | Deletes an existing document from Clicksign. |
| [Get Document](actions/get-document.md) | GET | Retrieves a document from Clicksign. |
| [List Documents](actions/list-documents.md) | GET | Retrieves documents from a Clicksign envelope. |
| [Update Document](actions/update-document.md) | PUT | Updates an existing document in Clicksign. |

### Document Event

| Action | Method | Description |
| --- | --- | --- |
| [List Document Events](actions/list-document-events.md) | GET | Retrieves events for a Clicksign document. |

### Envelope

| Action | Method | Description |
| --- | --- | --- |
| [Create Envelope](actions/create-envelope.md) | POST | Creates an envelope in Clicksign. |
| [Delete Envelope](actions/delete-envelope.md) | DELETE | Deletes an existing envelope from Clicksign. |
| [Get Envelope](actions/get-envelope.md) | GET | Retrieves an envelope from Clicksign. |
| [List Envelopes](actions/list-envelopes.md) | GET | Retrieves envelopes from Clicksign. |
| [Update Envelope](actions/update-envelope.md) | PUT | Updates an existing envelope in Clicksign. |

### Envelope Event

| Action | Method | Description |
| --- | --- | --- |
| [List Envelope Document Events](actions/list-envelope-document-events.md) | GET | Retrieves events for a Clicksign envelope. |

### Notification

| Action | Method | Description |
| --- | --- | --- |
| [Notify Envelope Signers](actions/notify-envelope-signers.md) | POST | Notifies signers for a Clicksign envelope. |

### Requirement

| Action | Method | Description |
| --- | --- | --- |
| [Create Authentication Requirement](actions/create-authentication-requirement.md) | POST | Creates an authentication requirement in Clicksign. |
| [Create Bulk Requirements](actions/create-bulk-requirements.md) | POST | Creates bulk requirements in a Clicksign envelope. |
| [Create Qualification Requirement](actions/create-qualification-requirement.md) | POST | Creates a qualification requirement in Clicksign. |
| [Delete Requirement](actions/delete-requirement.md) | DELETE | Deletes an existing requirement from Clicksign. |
| [Get Requirement](actions/get-requirement.md) | GET | Retrieves a requirement from Clicksign. |
| [List Requirements](actions/list-requirements.md) | GET | Retrieves requirements from a Clicksign envelope. |

### Signer

| Action | Method | Description |
| --- | --- | --- |
| [Create Signer](actions/create-signer.md) | POST | Creates a signer in a Clicksign envelope. |
| [Delete Signer](actions/delete-signer.md) | DELETE | Deletes an existing signer from Clicksign. |
| [Get Signer](actions/get-signer.md) | GET | Retrieves a signer from Clicksign. |
| [List Signers](actions/list-signers.md) | GET | Retrieves signers from a Clicksign envelope. |

