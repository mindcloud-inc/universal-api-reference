# <img src="https://images.mindcloud.co/apps/icons/images_1775494208884.png" alt="nandbox logo" width="28" height="28"> nandbox: Universal API

Draft mixed-transport nandbox wrapper with token auth scaffolding, required server connection fields, and media download support. Websocket bot methods and media upload remain blocked on current platform transport and raw-body limitations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/nandbox/latest
- **Category:** Communication / Team Messaging
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://nandbox.com/
- **Vendor API docs:** https://developer.nandbox.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Download Media File](actions/download-media-file.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nandbox/latest/actions/download-media-file?connectionId=$CONNECTION_ID&mediaId=123456789.jpg" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Download Media File](actions/download-media-file.md) | GET | Retrieves a media file from nandbox by media ID. |

