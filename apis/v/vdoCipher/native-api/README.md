# VdoCipher: Native API Reference

A consolidated summary of VdoCipher's API configuration and 26 documented operations, with links to official documentation.

- **Official docs:** https://www.vdocipher.com/page/api/
- **OpenAPI specification:** https://www.vdocipher.com/docs/swagger/schemas-swagger.json
- **API base URL:** `https://dev.vdocipher.com/api`

## Authentication

### API Secret

Authenticate with a VdoCipher API secret.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.vdocipher.com/docs/server/authorization)

## Endpoints (26 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Video Tags](actions/add-video-tags.md) | `POST /videos/tags/` | [docs](https://www.vdocipher.com/docs/swagger/index.html) |
| [Create Policy](actions/create-policy.md) | `POST /policy` | [docs](https://www.vdocipher.com/docs/swagger/index.html) |
| [Create Video OTP](actions/create-video-otp.md) | `POST /videos/:videoId/otp` | [docs](https://www.vdocipher.com/docs/server/playbackauth/otp) |
| [Create Video Upload Policy](actions/create-video-upload-policy.md) | `PUT /videos` | [docs](https://www.vdocipher.com/docs/server/upload/overview) |
| [Create Webhook](actions/create-webhook.md) | `POST /hooks/` | [docs](https://www.vdocipher.com/docs/swagger/index.html) |
| [Delete Policy](actions/delete-policy.md) | `DELETE /policy/:id` | [docs](https://www.vdocipher.com/docs/swagger/index.html) |
| [Delete Video](actions/delete-video.md) | `DELETE /videos` | [docs](https://www.vdocipher.com/docs/swagger/index.html) |
| [Delete Video File](actions/delete-video-file.md) | `DELETE /videos/:videoId/files/:fileId` | [docs](https://www.vdocipher.com/docs/swagger/index.html) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /hooks/` | [docs](https://www.vdocipher.com/docs/swagger/index.html) |
| [Get Video](actions/get-video.md) | `GET /videos/:videoId` | [docs](https://www.vdocipher.com/docs/swagger/index.html) |
| [Get Video Chapters](actions/get-video-chapters.md) | `GET /videos/:videoId/chapters` | [docs](https://www.vdocipher.com/docs/swagger/index.html) |
| [Get Video File Download Url](actions/get-video-file-download-url.md) | `GET /videos/:videoId/files/:fileId` | [docs](https://www.vdocipher.com/docs/swagger/index.html) |
| [Get Video Parameters](actions/get-video-parameters.md) | `GET /videos/:videoId/params` | [docs](https://www.vdocipher.com/docs/swagger/index.html) |
| [Import Video URL](actions/import-video-url.md) | `PUT /videos/importUrl` | [docs](https://www.vdocipher.com/docs/server/upload/import-url) |
| [List Policies](actions/list-policies.md) | `GET /policy` | [docs](https://www.vdocipher.com/docs/swagger/index.html) |
| [List Video Files](actions/list-video-files.md) | `GET /videos/:videoId/files` | [docs](https://www.vdocipher.com/docs/swagger/index.html) |
| [List Video Tags](actions/list-video-tags.md) | `GET /videos/tags/` | [docs](https://www.vdocipher.com/docs/swagger/index.html) |
| [List Videos](actions/list-videos.md) | `GET /videos` | [docs](https://www.vdocipher.com/docs/swagger/index.html) |
| [List Webhooks](actions/list-webhooks.md) | `GET /hooks/` | [docs](https://www.vdocipher.com/docs/swagger/index.html) |
| [Replace Video Upload Policy](actions/replace-video-upload-policy.md) | `PUT /videos/:videoId` | [docs](https://www.vdocipher.com/docs/server/upload/overview) |
| [Set Video Tags](actions/set-video-tags.md) | `PUT /videos/tags/` | [docs](https://www.vdocipher.com/docs/swagger/index.html) |
| [Update Policy](actions/update-policy.md) | `PUT /policy/:id` | [docs](https://www.vdocipher.com/docs/swagger/index.html) |
| [Update Video](actions/update-video.md) | `POST /videos/:videoId` | [docs](https://www.vdocipher.com/docs/swagger/index.html) |
| [Update Video Chapters](actions/update-video-chapters.md) | `PUT /videos/:videoId/chapters` | [docs](https://www.vdocipher.com/docs/swagger/index.html) |
| [Update Video Parameters](actions/update-video-parameters.md) | `POST /videos/:videoId/params` | [docs](https://www.vdocipher.com/docs/swagger/index.html) |
| [Upload Video File](actions/upload-video-file.md) | `POST /videos/:videoId/files` | [docs](https://www.vdocipher.com/docs/swagger/index.html) |
