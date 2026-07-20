# Restream: Native API Reference

A consolidated summary of Restream's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developers.restream.io
- **API base URL:** `https://api.restream.io/v2`

## Authentication

### OAuth2

Authorize MindCloud against Restream with OAuth2 authorization code and the frozen Restream scopes for profile, channels, stream, chat, clips, storage, and studio access.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://api.restream.io/login to approve access.
2. Exchange the returned authorization code with a POST request to https://api.restream.io/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `profile.read channels.read stream.read chat.read clips.read storage.read studio.read channels.write clips.write storage.write studio.write`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://api.restream.io/oauth/token.

[Official authentication documentation](https://developers.restream.io/authentication/)

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Channel](actions/add-channel.md) | `POST /user/channels` | [docs](https://developers.restream.io/channels/channel-add) |
| [Create Event Recording Download URL](actions/create-event-recording-download-url.md) | `POST /user/events/:eventId/recordings/download-url` | [docs](https://developers.restream.io/events/events-recording-download-url) |
| [Create Storage File Download URL](actions/create-storage-file-download-url.md) | `POST /user/storage/files/:fileId/download-url` | [docs](https://developers.restream.io/storage/storage-file-download-url) |
| [Delete Channel](actions/delete-channel.md) | `DELETE /user/channels/:channelId` | [docs](https://developers.restream.io/channels/channel-delete) |
| [Get Channel](actions/get-channel.md) | `GET /user/channels/:channelId` | [docs](https://developers.restream.io/channels/channel) |
| [Get Clip Download URL](actions/get-clip-download-url.md) | `GET /user/clips/:clipId/download` | [docs](https://developers.restream.io/clips/clips-download) |
| [Get Clip Project](actions/get-clip-project.md) | `GET /user/clips/projects/:projectId` | [docs](https://developers.restream.io/clips/clips-project-details) |
| [Get Event](actions/get-event.md) | `GET /user/events/:eventId` | [docs](https://developers.restream.io/events/event) |
| [Get Event Stream Key](actions/get-event-stream-key.md) | `GET /user/events/:eventId/streamKey` | [docs](https://developers.restream.io/events/event-stream-key) |
| [Get Profile](actions/get-profile.md) | `GET /user/profile` | [docs](https://developers.restream.io/private-api/profile) |
| [Get Storage File](actions/get-storage-file.md) | `GET /user/storage/files/:fileId` | [docs](https://developers.restream.io/storage/storage-file) |
| [Get Stream Key](actions/get-stream-key.md) | `GET /user/streamKey` | [docs](https://developers.restream.io/private-api/stream-key) |
| [List Channels](actions/list-channels.md) | `GET /user/channels` | [docs](https://developers.restream.io/channels/channels) |
| [List Clip Projects](actions/list-clip-projects.md) | `GET /user/clips/projects` | [docs](https://developers.restream.io/clips/clips-projects) |
| [List Event Recordings](actions/list-event-recordings.md) | `GET /user/events/:eventId/recordings` | [docs](https://developers.restream.io/events/events-recordings) |
| [List Events History](actions/list-events-history.md) | `GET /user/events/history` | [docs](https://developers.restream.io/events/events-history) |
| [List In Progress Events](actions/list-in-progress-events.md) | `GET /user/events/in-progress` | [docs](https://developers.restream.io/events/in-progress-events) |
| [List Storage Files](actions/list-storage-files.md) | `GET /user/storage/files` | [docs](https://developers.restream.io/storage/storage-files) |
| [List Studio Brands](actions/list-studio-brands.md) | `GET /user/studio/brands` | [docs](https://developers.restream.io/studio/studio-brands) |
| [List Studio Captions](actions/list-studio-captions.md) | `GET /user/studio/captions` | [docs](https://developers.restream.io/studio/studio-captions) |
| [List Studio QR Codes](actions/list-studio-qr-codes.md) | `GET /user/studio/qr-codes` | [docs](https://developers.restream.io/studio/studio-qr-codes) |
| [List Upcoming Events](actions/list-upcoming-events.md) | `GET /user/events/upcoming` | [docs](https://developers.restream.io/events/upcoming-events) |
| [Update Studio Caption](actions/update-studio-caption.md) | `PATCH /user/studio/captions/:captionId` | [docs](https://developers.restream.io/studio/studio-caption-update) |
| [Update Studio QR Code](actions/update-studio-qr-code.md) | `PATCH /user/studio/qr-codes/:qrCodeId` | [docs](https://developers.restream.io/studio/studio-qr-code-update) |
