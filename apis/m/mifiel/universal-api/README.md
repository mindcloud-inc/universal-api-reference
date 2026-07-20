# <img src="https://images.mindcloud.co/apps/icons/mifiel_1775138943260.png" alt="Mifiel logo" width="28" height="28"> Mifiel: Universal API

Manage signature documents, signers, webhooks, and signed artifacts in Mifiel

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mifiel/latest
- **Category:** Productivity / Legal & Contracts
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://app.mifiel.com
- **Vendor API docs:** https://docs.mifiel.com/en/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Webhooks](actions/list-webhooks.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mifiel/latest/actions/list-webhooks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Create Document](actions/create-document.md) | POST | Creates a new document in Mifiel. |
| [Delete Document](actions/delete-document.md) | DELETE | Deletes a document from Mifiel. |
| [Download Signed PDF](actions/download-signed-pdf.md) | GET | Retrieves a signed document PDF from Mifiel. |
| [Download XML](actions/download-xml.md) | GET | Retrieves a signed document XML file from Mifiel. |
| [Download ZIP File](actions/download-zip-file.md) | GET | Retrieves a signed document ZIP archive from Mifiel. |
| [Get Document](actions/get-document.md) | GET | Retrieves a document from Mifiel. |

### Query

| Action | Method | Description |
| --- | --- | --- |
| [Search Advanced Information](actions/search-advanced-information.md) | GET | Searches advanced document information in Mifiel. |

### Stakeholder

| Action | Method | Description |
| --- | --- | --- |
| [Create Stakeholder](actions/create-stakeholder.md) | POST | Creates a stakeholder for a document in Mifiel. |
| [Delete Stakeholder](actions/delete-stakeholder.md) | DELETE | Deletes a stakeholder from a document in Mifiel. |
| [Update Stakeholder](actions/update-stakeholder.md) | PUT | Updates a stakeholder for a document in Mifiel. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook endpoint in Mifiel. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes a webhook endpoint from Mifiel. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhook endpoint records from Mifiel. |

