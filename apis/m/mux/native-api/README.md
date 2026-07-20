# Mux: Native API Reference

A consolidated summary of Mux's API configuration and 59 documented operations, with links to official documentation.

- **Official docs:** https://www.mux.com/docs/core/mux-fundamentals
- **OpenAPI specification:** https://mux.com/api-spec.json
- **API base URL:** `https://api.mux.com`

## Authentication

### Mux Basic Auth

Use your Mux Access Token ID as the username and Secret Key as the password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://www.mux.com/docs/core/mux-fundamentals)

## Pagination

Use `limit` in the query string to set the page size (default 25; minimum 1). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (59 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Direct Upload](actions/cancel-direct-upload.md) | `PUT /video/v1/uploads/{UPLOAD_ID}/cancel` | [docs](https://www.mux.com/docs/api-reference/video/direct-uploads) |
| [Create a Live Stream](actions/create-a-live-stream.md) | `POST /video/v1/live-streams` | [docs](https://www.mux.com/docs/api-reference/video/live-streams) |
| [Create an Asset](actions/create-an-asset.md) | `POST /video/v1/assets` | [docs](https://www.mux.com/docs/api-reference/video/assets) |
| [Create Asset Playback ID](actions/create-asset-playback-id.md) | `POST /video/v1/assets/{ASSET_ID}/playback-ids` | [docs](https://www.mux.com/docs/api-reference/video/assets) |
| [Create Asset Static Rendition](actions/create-asset-static-rendition.md) | `POST /video/v1/assets/{ASSET_ID}/static-renditions` | [docs](https://www.mux.com/docs/api-reference/video/assets) |
| [Create Asset Track](actions/create-asset-track.md) | `POST /video/v1/assets/{ASSET_ID}/tracks` | [docs](https://www.mux.com/docs/api-reference/video/assets) |
| [Create Direct Upload](actions/create-direct-upload.md) | `POST /video/v1/uploads` | [docs](https://www.mux.com/docs/api-reference/video/direct-uploads) |
| [Create Live Stream Playback ID](actions/create-live-stream-playback-id.md) | `POST /video/v1/live-streams/{LIVE_STREAM_ID}/playback-ids` | [docs](https://www.mux.com/docs/api-reference/video/live-streams) |
| [Create Live Stream Simulcast Target](actions/create-live-stream-simulcast-target.md) | `POST /video/v1/live-streams/{LIVE_STREAM_ID}/simulcast-targets` | [docs](https://www.mux.com/docs/api-reference/video/live-streams) |
| [Create Playback Restriction](actions/create-playback-restriction.md) | `POST /video/v1/playback-restrictions` | [docs](https://www.mux.com/docs/api-reference/video/playback-restrictions) |
| [Create Transcription Vocabulary](actions/create-transcription-vocabulary.md) | `POST /video/v1/transcription-vocabularies` | [docs](https://www.mux.com/docs/api-reference/video/transcription-vocabularies) |
| [Create URL Signing Key](actions/create-url-signing-key.md) | `POST /video/v1/signing-keys` | [docs](https://www.mux.com/docs/api-reference/video/signing-keys) |
| [Delete a Live Stream](actions/delete-a-live-stream.md) | `DELETE /video/v1/live-streams/{LIVE_STREAM_ID}` | [docs](https://www.mux.com/docs/api-reference/video/live-streams) |
| [Delete an Asset](actions/delete-an-asset.md) | `DELETE /video/v1/assets/{ASSET_ID}` | [docs](https://www.mux.com/docs/api-reference/video/assets) |
| [Delete Asset Playback ID](actions/delete-asset-playback-id.md) | `DELETE /video/v1/assets/{ASSET_ID}/playback-ids/{PLAYBACK_ID}` | [docs](https://www.mux.com/docs/api-reference/video/assets) |
| [Delete Asset Static Rendition](actions/delete-asset-static-rendition.md) | `DELETE /video/v1/assets/{ASSET_ID}/static-renditions/{STATIC_RENDITION_ID}` | [docs](https://www.mux.com/docs/api-reference/video/assets) |
| [Delete Asset Track](actions/delete-asset-track.md) | `DELETE /video/v1/assets/{ASSET_ID}/tracks/{TRACK_ID}` | [docs](https://www.mux.com/docs/api-reference/video/assets) |
| [Delete Live Stream New Asset Static Renditions](actions/delete-live-stream-new-asset-static-renditions.md) | `DELETE /video/v1/live-streams/{LIVE_STREAM_ID}/new-asset-settings/static-renditions` | [docs](https://www.mux.com/docs/api-reference/video/live-streams) |
| [Delete Live Stream Playback ID](actions/delete-live-stream-playback-id.md) | `DELETE /video/v1/live-streams/{LIVE_STREAM_ID}/playback-ids/{PLAYBACK_ID}` | [docs](https://www.mux.com/docs/api-reference/video/live-streams) |
| [Delete Live Stream Simulcast Target](actions/delete-live-stream-simulcast-target.md) | `DELETE /video/v1/live-streams/{LIVE_STREAM_ID}/simulcast-targets/{SIMULCAST_TARGET_ID}` | [docs](https://www.mux.com/docs/api-reference/video/live-streams) |
| [Delete Playback Restriction](actions/delete-playback-restriction.md) | `DELETE /video/v1/playback-restrictions/{PLAYBACK_RESTRICTION_ID}` | [docs](https://www.mux.com/docs/api-reference/video/playback-restrictions) |
| [Delete Transcription Vocabulary](actions/delete-transcription-vocabulary.md) | `DELETE /video/v1/transcription-vocabularies/{TRANSCRIPTION_VOCABULARY_ID}` | [docs](https://www.mux.com/docs/api-reference/video/transcription-vocabularies) |
| [Delete URL Signing Key](actions/delete-url-signing-key.md) | `DELETE /video/v1/signing-keys/{SIGNING_KEY_ID}` | [docs](https://www.mux.com/docs/api-reference/video/signing-keys) |
| [Disable a Live Stream](actions/disable-a-live-stream.md) | `PUT /video/v1/live-streams/{LIVE_STREAM_ID}/disable` | [docs](https://www.mux.com/docs/api-reference/video/live-streams) |
| [Enable a Live Stream](actions/enable-a-live-stream.md) | `PUT /video/v1/live-streams/{LIVE_STREAM_ID}/enable` | [docs](https://www.mux.com/docs/api-reference/video/live-streams) |
| [Generate Asset Track Subtitles](actions/generate-asset-track-subtitles.md) | `POST /video/v1/assets/{ASSET_ID}/tracks/{TRACK_ID}/generate-subtitles` | [docs](https://www.mux.com/docs/api-reference/video/assets) |
| [List Assets](actions/list-assets.md) | `GET /video/v1/assets` | [docs](https://www.mux.com/docs/api-reference/video/assets/list-assets) |
| [List Delivery Usage](actions/list-delivery-usage.md) | `GET /video/v1/delivery-usage` | [docs](https://www.mux.com/docs/api-reference/video/delivery-usage) |
| [List Direct Uploads](actions/list-direct-uploads.md) | `GET /video/v1/uploads` | [docs](https://www.mux.com/docs/api-reference/video/direct-uploads) |
| [List DRM Configurations](actions/list-drm-configurations.md) | `GET /video/v1/drm-configurations` | [docs](https://www.mux.com/docs/api-reference/video/drm-configurations) |
| [List Live Streams](actions/list-live-streams.md) | `GET /video/v1/live-streams` | [docs](https://www.mux.com/docs/api-reference/video/live-streams) |
| [List Playback Restrictions](actions/list-playback-restrictions.md) | `GET /video/v1/playback-restrictions` | [docs](https://www.mux.com/docs/api-reference/video/playback-restrictions) |
| [List Transcription Vocabularies](actions/list-transcription-vocabularies.md) | `GET /video/v1/transcription-vocabularies` | [docs](https://www.mux.com/docs/api-reference/video/transcription-vocabularies) |
| [List URL Signing Keys](actions/list-url-signing-keys.md) | `GET /video/v1/signing-keys` | [docs](https://www.mux.com/docs/api-reference/video/signing-keys) |
| [Reset Live Stream Key](actions/reset-live-stream-key.md) | `POST /video/v1/live-streams/{LIVE_STREAM_ID}/reset-stream-key` | [docs](https://www.mux.com/docs/api-reference/video/live-streams) |
| [Retrieve a Live Stream](actions/retrieve-a-live-stream.md) | `GET /video/v1/live-streams/{LIVE_STREAM_ID}` | [docs](https://www.mux.com/docs/api-reference/video/live-streams) |
| [Retrieve an Asset](actions/retrieve-an-asset.md) | `GET /video/v1/assets/{ASSET_ID}` | [docs](https://www.mux.com/docs/api-reference/video/assets) |
| [Retrieve Asset Input Info](actions/retrieve-asset-input-info.md) | `GET /video/v1/assets/{ASSET_ID}/input-info` | [docs](https://www.mux.com/docs/api-reference/video/assets) |
| [Retrieve Asset Playback ID](actions/retrieve-asset-playback-id.md) | `GET /video/v1/assets/{ASSET_ID}/playback-ids/{PLAYBACK_ID}` | [docs](https://www.mux.com/docs/api-reference/video/assets) |
| [Retrieve Direct Upload](actions/retrieve-direct-upload.md) | `GET /video/v1/uploads/{UPLOAD_ID}` | [docs](https://www.mux.com/docs/api-reference/video/direct-uploads) |
| [Retrieve DRM Configuration](actions/retrieve-drm-configuration.md) | `GET /video/v1/drm-configurations/{DRM_CONFIGURATION_ID}` | [docs](https://www.mux.com/docs/api-reference/video/drm-configurations) |
| [Retrieve Live Stream Playback ID](actions/retrieve-live-stream-playback-id.md) | `GET /video/v1/live-streams/{LIVE_STREAM_ID}/playback-ids/{PLAYBACK_ID}` | [docs](https://www.mux.com/docs/api-reference/video/live-streams) |
| [Retrieve Live Stream Simulcast Target](actions/retrieve-live-stream-simulcast-target.md) | `GET /video/v1/live-streams/{LIVE_STREAM_ID}/simulcast-targets/{SIMULCAST_TARGET_ID}` | [docs](https://www.mux.com/docs/api-reference/video/live-streams) |
| [Retrieve Playback ID Owner](actions/retrieve-playback-id-owner.md) | `GET /video/v1/playback-ids/{PLAYBACK_ID}` | [docs](https://www.mux.com/docs/api-reference/video/playback-ids) |
| [Retrieve Playback Restriction](actions/retrieve-playback-restriction.md) | `GET /video/v1/playback-restrictions/{PLAYBACK_RESTRICTION_ID}` | [docs](https://www.mux.com/docs/api-reference/video/playback-restrictions) |
| [Retrieve Transcription Vocabulary](actions/retrieve-transcription-vocabulary.md) | `GET /video/v1/transcription-vocabularies/{TRANSCRIPTION_VOCABULARY_ID}` | [docs](https://www.mux.com/docs/api-reference/video/transcription-vocabularies) |
| [Retrieve URL Signing Key](actions/retrieve-url-signing-key.md) | `GET /video/v1/signing-keys/{SIGNING_KEY_ID}` | [docs](https://www.mux.com/docs/api-reference/video/signing-keys) |
| [Signal Live Stream Complete](actions/signal-live-stream-complete.md) | `PUT /video/v1/live-streams/{LIVE_STREAM_ID}/complete` | [docs](https://www.mux.com/docs/api-reference/video/live-streams) |
| [Update a Live Stream](actions/update-a-live-stream.md) | `PATCH /video/v1/live-streams/{LIVE_STREAM_ID}` | [docs](https://www.mux.com/docs/api-reference/video/live-streams) |
| [Update an Asset](actions/update-an-asset.md) | `PATCH /video/v1/assets/{ASSET_ID}` | [docs](https://www.mux.com/docs/api-reference/video/assets) |
| [Update Asset Master Access](actions/update-asset-master-access.md) | `PUT /video/v1/assets/{ASSET_ID}/master-access` | [docs](https://www.mux.com/docs/api-reference/video/assets) |
| [Update Asset MP4 Support](actions/update-asset-mp4-support.md) | `PUT /video/v1/assets/{ASSET_ID}/mp4-support` | [docs](https://www.mux.com/docs/api-reference/video/assets) |
| [Update Asset Track](actions/update-asset-track.md) | `PATCH /video/v1/assets/{ASSET_ID}/tracks/{TRACK_ID}` | [docs](https://www.mux.com/docs/api-reference/video/assets) |
| [Update Live Stream Embedded Subtitles](actions/update-live-stream-embedded-subtitles.md) | `PUT /video/v1/live-streams/{LIVE_STREAM_ID}/embedded-subtitles` | [docs](https://www.mux.com/docs/api-reference/video/live-streams) |
| [Update Live Stream Generated Subtitles](actions/update-live-stream-generated-subtitles.md) | `PUT /video/v1/live-streams/{LIVE_STREAM_ID}/generated-subtitles` | [docs](https://www.mux.com/docs/api-reference/video/live-streams) |
| [Update Live Stream New Asset Static Renditions](actions/update-live-stream-new-asset-static-renditions.md) | `PUT /video/v1/live-streams/{LIVE_STREAM_ID}/new-asset-settings/static-renditions` | [docs](https://www.mux.com/docs/api-reference/video/live-streams) |
| [Update Referrer Playback Restriction](actions/update-referrer-playback-restriction.md) | `PUT /video/v1/playback-restrictions/{PLAYBACK_RESTRICTION_ID}/referrer` | [docs](https://www.mux.com/docs/api-reference/video/playback-restrictions) |
| [Update Transcription Vocabulary](actions/update-transcription-vocabulary.md) | `PUT /video/v1/transcription-vocabularies/{TRANSCRIPTION_VOCABULARY_ID}` | [docs](https://www.mux.com/docs/api-reference/video/transcription-vocabularies) |
| [Update User Agent Restriction](actions/update-user-agent-restriction.md) | `PUT /video/v1/playback-restrictions/{PLAYBACK_RESTRICTION_ID}/user_agent` | [docs](https://www.mux.com/docs/api-reference/video/playback-restrictions) |
