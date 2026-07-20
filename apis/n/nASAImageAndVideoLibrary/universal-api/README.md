# <img src="https://images.mindcloud.co/apps/icons/n-asaimage-and-video-library_1777575943284.png" alt="NASA Image and Video Library logo" width="28" height="28"> NASA Image and Video Library: Universal API

Search and retrieve NASA images, videos, audio, and metadata

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/nASAImageAndVideoLibrary/latest
- **Category:** Content & Files / Storage
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://images.nasa.gov
- **Vendor API docs:** https://images.nasa.gov/docs/images.nasa.gov_api_docs.pdf

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Album Contents](actions/get-album-contents.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nASAImageAndVideoLibrary/latest/actions/get-album-contents?connectionId=$CONNECTION_ID&albumName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Asset

| Action | Method | Description |
| --- | --- | --- |
| [Get Album Contents](actions/get-album-contents.md) | GET | Retrieves album contents from NASA Image and Video Library. |
| [Get Asset Manifest](actions/get-asset-manifest.md) | GET | Retrieves an asset manifest from NASA Image and Video Library. |
| [Get Asset Metadata Location](actions/get-asset-metadata-location.md) | GET | Retrieves an asset metadata URL from NASA Image and Video Library. |
| [Get Video Captions Location](actions/get-video-captions-location.md) | GET | Retrieves a video captions URL from NASA Image and Video Library. |
| [Search Assets](actions/search-assets.md) | GET | Finds assets in NASA Image and Video Library by search criteria. |

