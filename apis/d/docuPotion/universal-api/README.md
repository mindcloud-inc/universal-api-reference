# <img src="https://images.mindcloud.co/apps/icons/docu-potion_1775837969397.png" alt="DocuPotion logo" width="28" height="28"> DocuPotion: Universal API

Create templates and generate PDF documents from your data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/docuPotion/latest
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://docupotion.com
- **Vendor API docs:** https://docupotion.com/api-docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docuPotion/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET |  |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Create Document](actions/create-document.md) | POST |  |
| [Create Document to Connected S3](actions/create-document-to-connected-s3.md) | POST |  |
| [Create PDF Base64](actions/create-pdf-base64.md) | POST |  |
| [Create PDF URL](actions/create-pdf-url.md) | POST |  |
| [Create PNG Base64](actions/create-png-base64.md) | POST |  |
| [Create PNG URL](actions/create-png-url.md) | POST |  |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [List Templates](actions/list-templates.md) | GET |  |

