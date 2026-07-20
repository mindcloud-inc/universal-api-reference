# <img src="https://images.mindcloud.co/apps/icons/boloforms_1774637533129.png" alt="BoloForms logo" width="28" height="28"> BoloForms: Universal API

Send, sign, and track documents with BoloSign by BoloForms using an API key plus workspace-scoped requests.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/boloForms/latest
- **Category:** Productivity / Legal & Contracts
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.boloforms.com/
- **Vendor API docs:** https://developer.boloforms.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Documents](actions/list-documents.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/boloForms/latest/actions/list-documents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Document

| Action | Method | Description |
| --- | --- | --- |
| [List Documents](actions/list-documents.md) | GET | Retrieves documents from BoloForms. |

### Form Response

| Action | Method | Description |
| --- | --- | --- |
| [Get Form Responses](actions/get-form-responses.md) | GET | Retrieves responses from a BoloForms form. |

### Signature Request

| Action | Method | Description |
| --- | --- | --- |
| [Send Template For Signing](actions/send-template-for-signing.md) | POST | Sends a BoloForms template for signing. |

### Template Respondent

| Action | Method | Description |
| --- | --- | --- |
| [Get Template Respondents](actions/get-template-respondents.md) | GET | Retrieves respondents for a BoloForms template. |

