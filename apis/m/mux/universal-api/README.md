# <img src="https://images.mindcloud.co/apps/icons/mux-icon-square-1024_1775762830582.png" alt="Mux logo" width="28" height="28"> Mux: Universal API

Mux provides APIs for video assets, live streams, direct uploads, playback restrictions, URL signing keys, delivery usage, DRM configurations, and transcription vocabularies.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mux/latest
- **Actions:** 59
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.mux.com/
- **Vendor API docs:** https://www.mux.com/docs/core/mux-fundamentals

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Assets](actions/list-assets.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mux/latest/actions/list-assets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (59)

### Asset

| Action | Method | Description |
| --- | --- | --- |
| [List Assets](actions/list-assets.md) | GET |  |

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [Create an Asset](actions/create-an-asset.md) | POST |  |
| [Create Asset Playback ID](actions/create-asset-playback-id.md) | POST |  |
| [Create Asset Static Rendition](actions/create-asset-static-rendition.md) | POST |  |
| [Create Asset Track](actions/create-asset-track.md) | POST |  |
| [Delete an Asset](actions/delete-an-asset.md) | DELETE |  |
| [Delete Asset Playback ID](actions/delete-asset-playback-id.md) | DELETE |  |
| [Delete Asset Static Rendition](actions/delete-asset-static-rendition.md) | DELETE |  |
| [Delete Asset Track](actions/delete-asset-track.md) | DELETE |  |
| [Generate Asset Track Subtitles](actions/generate-asset-track-subtitles.md) | POST |  |
| [Retrieve an Asset](actions/retrieve-an-asset.md) | GET |  |
| [Retrieve Asset Input Info](actions/retrieve-asset-input-info.md) | GET |  |
| [Retrieve Asset Playback ID](actions/retrieve-asset-playback-id.md) | GET |  |
| [Update an Asset](actions/update-an-asset.md) | PUT |  |
| [Update Asset Master Access](actions/update-asset-master-access.md) | PUT |  |
| [Update Asset MP4 Support](actions/update-asset-mp4-support.md) | PUT |  |
| [Update Asset Track](actions/update-asset-track.md) | PUT |  |

### Datasets

| Action | Method | Description |
| --- | --- | --- |
| [Create Transcription Vocabulary](actions/create-transcription-vocabulary.md) | POST |  |
| [Delete Transcription Vocabulary](actions/delete-transcription-vocabulary.md) | DELETE |  |
| [List Transcription Vocabularies](actions/list-transcription-vocabularies.md) | GET |  |
| [Retrieve Transcription Vocabulary](actions/retrieve-transcription-vocabulary.md) | GET |  |
| [Update Transcription Vocabulary](actions/update-transcription-vocabulary.md) | PUT |  |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Direct Upload](actions/cancel-direct-upload.md) | PUT |  |
| [Create Direct Upload](actions/create-direct-upload.md) | POST |  |
| [List Direct Uploads](actions/list-direct-uploads.md) | GET |  |
| [Retrieve Direct Upload](actions/retrieve-direct-upload.md) | GET |  |

### Policies

| Action | Method | Description |
| --- | --- | --- |
| [Create Playback Restriction](actions/create-playback-restriction.md) | POST |  |
| [Delete Playback Restriction](actions/delete-playback-restriction.md) | DELETE |  |
| [List DRM Configurations](actions/list-drm-configurations.md) | GET |  |
| [List Playback Restrictions](actions/list-playback-restrictions.md) | GET |  |
| [Retrieve DRM Configuration](actions/retrieve-drm-configuration.md) | GET |  |
| [Retrieve Playback Restriction](actions/retrieve-playback-restriction.md) | GET |  |
| [Update Referrer Playback Restriction](actions/update-referrer-playback-restriction.md) | PUT |  |
| [Update User Agent Restriction](actions/update-user-agent-restriction.md) | PUT |  |

### Recordings

| Action | Method | Description |
| --- | --- | --- |
| [Create a Live Stream](actions/create-a-live-stream.md) | POST |  |
| [Create Live Stream Playback ID](actions/create-live-stream-playback-id.md) | POST |  |
| [Create Live Stream Simulcast Target](actions/create-live-stream-simulcast-target.md) | POST |  |
| [Delete a Live Stream](actions/delete-a-live-stream.md) | DELETE |  |
| [Delete Live Stream New Asset Static Renditions](actions/delete-live-stream-new-asset-static-renditions.md) | DELETE |  |
| [Delete Live Stream Playback ID](actions/delete-live-stream-playback-id.md) | DELETE |  |
| [Delete Live Stream Simulcast Target](actions/delete-live-stream-simulcast-target.md) | DELETE |  |
| [Disable a Live Stream](actions/disable-a-live-stream.md) | PUT |  |
| [Enable a Live Stream](actions/enable-a-live-stream.md) | PUT |  |
| [List Live Streams](actions/list-live-streams.md) | GET |  |
| [Reset Live Stream Key](actions/reset-live-stream-key.md) | PUT |  |
| [Retrieve a Live Stream](actions/retrieve-a-live-stream.md) | GET |  |
| [Retrieve Live Stream Playback ID](actions/retrieve-live-stream-playback-id.md) | GET |  |
| [Retrieve Live Stream Simulcast Target](actions/retrieve-live-stream-simulcast-target.md) | GET |  |
| [Retrieve Playback ID Owner](actions/retrieve-playback-id-owner.md) | GET |  |
| [Signal Live Stream Complete](actions/signal-live-stream-complete.md) | PUT |  |
| [Update a Live Stream](actions/update-a-live-stream.md) | PUT |  |
| [Update Live Stream Embedded Subtitles](actions/update-live-stream-embedded-subtitles.md) | PUT |  |
| [Update Live Stream Generated Subtitles](actions/update-live-stream-generated-subtitles.md) | PUT |  |
| [Update Live Stream New Asset Static Renditions](actions/update-live-stream-new-asset-static-renditions.md) | PUT |  |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [List Delivery Usage](actions/list-delivery-usage.md) | GET |  |

### Secrets

| Action | Method | Description |
| --- | --- | --- |
| [Create URL Signing Key](actions/create-url-signing-key.md) | POST |  |
| [Delete URL Signing Key](actions/delete-url-signing-key.md) | DELETE |  |
| [List URL Signing Keys](actions/list-url-signing-keys.md) | GET |  |
| [Retrieve URL Signing Key](actions/retrieve-url-signing-key.md) | GET |  |

