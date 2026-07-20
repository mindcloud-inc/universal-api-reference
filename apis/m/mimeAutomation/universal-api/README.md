# <img src="https://images.mindcloud.co/apps/icons/nadles-icon_1777566025094.jpeg" alt="Mime Automation logo" width="28" height="28"> Mime Automation: Universal API

Extract attachments from base64-encoded EML and TNEF files using the Mime Automation API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mimeAutomation/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.accloudsolutions.com
- **Vendor API docs:** https://learn.microsoft.com/en-us/connectors/mimeautomationip/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Extract Files From TNEF](actions/extract-files-from-tnef.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mimeAutomation/latest/actions/extract-files-from-tnef?connectionId=$CONNECTION_ID&content=Paste%20base64-encoded%20TNEF%20content" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Extract Files From TNEF](actions/extract-files-from-tnef.md) | GET | Retrieves attachments from a TNEF-encoded file in Mime Automation. |

### Mime Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Extract Files From EML](actions/extract-files-from-eml.md) | GET | Retrieves attachments from a base64-encoded EML file in Mime Automation. |

