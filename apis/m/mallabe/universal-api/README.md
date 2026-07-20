# <img src="https://images.mindcloud.co/apps/icons/mallabe_1773930074653.png" alt="Mallabe logo" width="28" height="28"> Mallabe: Universal API

Process images, upload files, inspect websites, convert currencies, and parse user agents

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mallabe/latest
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.mallabe.com
- **Vendor API docs:** https://rapidapi.com/mallabe1/api/mallabe

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Image Metadata](actions/get-image-metadata.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mallabe/latest/actions/get-image-metadata?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Currency

| Action | Method | Description |
| --- | --- | --- |
| [Convert Currency](actions/convert-currency.md) | GET | Retrieves a currency conversion from Mallabe. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Upload File](actions/upload-file.md) | POST | Uploads a file to Mallabe for hosting. |

### Image

| Action | Method | Description |
| --- | --- | --- |
| [Compress Image](actions/compress-image.md) | POST | Creates a compressed image in Mallabe. |
| [Get Image Metadata](actions/get-image-metadata.md) | GET | Retrieves metadata for an image from Mallabe. |
| [Resize Image](actions/resize-image.md) | POST | Creates a resized image in Mallabe. |

### User Agent

| Action | Method | Description |
| --- | --- | --- |
| [Parse User Agent](actions/parse-user-agent.md) | GET | Retrieves parsed user agent details from Mallabe. |

### Website

| Action | Method | Description |
| --- | --- | --- |
| [Get Website Status](actions/get-website-status.md) | GET | Retrieves website status details from Mallabe. |
| [Get Website Thumbnail](actions/get-website-thumbnail.md) | GET | Retrieves a website thumbnail from Mallabe. |

