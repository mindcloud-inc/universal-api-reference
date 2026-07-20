# <img src="https://images.mindcloud.co/apps/icons/cloudmersive-icon_1777490428127.png" alt="Cloudmersive Video and Media logo" width="28" height="28"> Cloudmersive Video and Media: Universal API

Convert, resize, edit, and inspect audio and video

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cloudmersiveVideoAndMedia/latest
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://cloudmersive.com/video-and-media-services-api
- **Vendor API docs:** https://api.cloudmersive.com/docs/video.asp

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Media Information](actions/get-media-information.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersiveVideoAndMedia/latest/actions/get-media-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Audio File

| Action | Method | Description |
| --- | --- | --- |
| [Convert Audio to MP3](actions/convert-audio-to-mp3.md) | GET | Converts an audio file to MP3 in Cloudmersive Video and Media. |

### Media Information

| Action | Method | Description |
| --- | --- | --- |
| [Get Media Information](actions/get-media-information.md) | GET | Retrieves media information from Cloudmersive Video and Media. |

