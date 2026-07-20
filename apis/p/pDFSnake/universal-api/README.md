# <img src="https://images.mindcloud.co/apps/icons/pdf-snake-icon-192_1775840378138.png" alt="PDF Snake logo" width="28" height="28"> PDF Snake: Universal API

Impose PDF, PNG, and JPEG files into booklets, business cards, and other print layouts through the PDF Snake Web API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pDFSnake/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.pdfsnake.com/
- **Vendor API docs:** https://www.pdfsnake.com/tutorials/web-api.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Byte Balance](actions/get-byte-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDFSnake/latest/actions/get-byte-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Byte Balance](actions/get-byte-balance.md) | GET | Retrieves your current byte balance from PDF Snake. |

### Imposed File

| Action | Method | Description |
| --- | --- | --- |
| [Impose Document](actions/impose-document.md) | POST | Creates an imposed document from uploaded files in PDF Snake. |

