# <img src="https://images.mindcloud.co/apps/icons/chatpdf-icon_1775847811127.png" alt="ChatPDF logo" width="28" height="28"> ChatPDF: Universal API

ChatPDF lets you upload PDFs or add them by URL, then ask questions against each source and optionally retrieve reference pages used in the answer.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/chatPDF/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.chatpdf.com
- **Vendor API docs:** https://www.chatpdf.com/docs/api/backend

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Send Chat Message](actions/send-chat-message.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatPDF/latest/actions/send-chat-message?connectionId=$CONNECTION_ID&sourceId=src_xxxxxx&messages%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Chat Reply

| Action | Method | Description |
| --- | --- | --- |
| [Send Chat Message](actions/send-chat-message.md) | GET |  |
| [Send Chat Message With References](actions/send-chat-message-with-references.md) | GET |  |
| [Stream Chat Message](actions/stream-chat-message.md) | GET |  |

### Pdf Source

| Action | Method | Description |
| --- | --- | --- |
| [Add PDF From URL](actions/add-pdf-from-url.md) | POST |  |
| [Delete PDF Sources](actions/delete-pdf-sources.md) | DELETE |  |
| [Upload PDF File](actions/upload-pdf-file.md) | POST |  |

