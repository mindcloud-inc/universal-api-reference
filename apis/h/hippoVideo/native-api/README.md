# Hippo Video: Native API Reference

A consolidated summary of Hippo Video's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://help.hippovideo.io/support/solutions/folders/19000163093
- **API base URL:** `https://www.hippovideo.io`

## Authentication

### Email + API Key Token Bootstrap

Uses the Hippo Video account email and API key to mint an authentication token for API requests.

### Credentials

- **Email:** `email` · required · Hippo Video account email address
- **API Key:** `apiKey` · required · Hippo Video API key from profile settings

[Official authentication documentation](https://help.hippovideo.io/support/solutions/articles/19000095978-api-authorization)

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Generate Bulk Personalized Video Tracking IDs](actions/generate-bulk-personalized-video-tracking-ids.md) | `POST /api/v1/me/video/bulk_personalize` | [docs](https://help.hippovideo.io/support/solutions/articles/19000099793-bulk-video-personalization-and-tracking-api) |
| [Generate Personalized Videos](actions/generate-personalized-videos.md) | `POST /api/v1/me/video/personalize` | [docs](https://help.hippovideo.io/support/solutions/articles/19000095986-generate-personalized-videos-through-api) |
| [Generate Video Ticket Guest URL](actions/generate-video-ticket-guest-url.md) | `GET /api/v1/me/video/guest_url/` | [docs](https://help.hippovideo.io/support/solutions/articles/19000116131-video-tickets-api) |
| [Get Transcoded Video Download URL](actions/get-transcoded-video-download-url.md) | `POST /video/transcoded/signed_url` | [docs](https://help.hippovideo.io/support/solutions/articles/19000158930-transcoded-video-download-api) |
| [Get Video Details](actions/get-video-details.md) | `GET /api/v1/me/video/:video_id` | [docs](https://help.hippovideo.io/support/solutions/articles/19000095982-video-details-api) |
| [Get Video Reports](actions/get-video-reports.md) | `GET /api/v1/me/video/reports/:video_id` | [docs](https://help.hippovideo.io/support/solutions/articles/19000095984-video-reports-api) |
| [Get Viewer Profile by Lead Email](actions/get-viewer-profile-by-lead-email.md) | `GET /api/v1/me/video/viewer_profile` | [docs](https://help.hippovideo.io/support/solutions/articles/19000095984-video-reports-api) |
| [Get Viewer Profile by Video](actions/get-viewer-profile-by-video.md) | `GET /api/v1/me/video/viewer_profile` | [docs](https://help.hippovideo.io/support/solutions/articles/19000095984-video-reports-api) |
| [Import Video](actions/import-video.md) | `POST /api/v1/me/video/import` | [docs](https://help.hippovideo.io/support/solutions/articles/19000100703-import-api) |
| [List Video Categories](actions/list-video-categories.md) | `GET /api/v1/me/video/categories` | [docs](https://help.hippovideo.io/support/solutions/articles/19000095979-categories-api) |
| [List Videos](actions/list-videos.md) | `GET /api/v1/me/videos/list` | [docs](https://help.hippovideo.io/support/solutions/articles/19000095981-video-library-api) |
