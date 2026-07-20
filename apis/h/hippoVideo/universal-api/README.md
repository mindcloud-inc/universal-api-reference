# <img src="https://images.mindcloud.co/apps/icons/hippo-video_1775568699673.png" alt="Hippo Video logo" width="28" height="28"> Hippo Video: Universal API

Create, personalize, share, and track videos

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/hippoVideo/latest
- **Category:** Marketing
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.hippovideo.io
- **Vendor API docs:** https://help.hippovideo.io/support/solutions/folders/19000163093

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Video Categories](actions/list-video-categories.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hippoVideo/latest/actions/list-video-categories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Personalized Video

| Action | Method | Description |
| --- | --- | --- |
| [Generate Personalized Videos](actions/generate-personalized-videos.md) | POST | Creates personalized videos in Hippo Video. |

### Personalized Video Tracking Batch

| Action | Method | Description |
| --- | --- | --- |
| [Generate Bulk Personalized Video Tracking IDs](actions/generate-bulk-personalized-video-tracking-ids.md) | POST | Creates bulk personalized video tracking IDs in Hippo Video. |

### Transcoded Video

| Action | Method | Description |
| --- | --- | --- |
| [Get Transcoded Video Download URL](actions/get-transcoded-video-download-url.md) | GET | Retrieves a download URL for a transcoded Hippo Video archive. |

### Video

| Action | Method | Description |
| --- | --- | --- |
| [Get Video Details](actions/get-video-details.md) | GET | Retrieves details for a Hippo Video video. |
| [Import Video](actions/import-video.md) | POST | Imports a video into Hippo Video from a downloadable URL. |
| [List Videos](actions/list-videos.md) | GET | Retrieves videos from the Hippo Video library. |

### Video Category

| Action | Method | Description |
| --- | --- | --- |
| [List Video Categories](actions/list-video-categories.md) | GET | Retrieves video categories from Hippo Video. |

### Video Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Video Reports](actions/get-video-reports.md) | GET | Retrieves reports for a Hippo Video video. |

### Video Ticket

| Action | Method | Description |
| --- | --- | --- |
| [Generate Video Ticket Guest URL](actions/generate-video-ticket-guest-url.md) | GET | Retrieves a guest URL for Hippo Video ticket recording. |

### Viewer Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get Viewer Profile by Lead Email](actions/get-viewer-profile-by-lead-email.md) | GET | Retrieves viewer profiles in Hippo Video by lead email. |
| [Get Viewer Profile by Video](actions/get-viewer-profile-by-video.md) | GET | Retrieves viewer profiles for a Hippo Video video. |

