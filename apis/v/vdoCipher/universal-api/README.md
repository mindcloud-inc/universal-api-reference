# <img src="https://images.mindcloud.co/apps/icons/vdo-cipher_1775957558932.png" alt="VdoCipher logo" width="28" height="28"> VdoCipher: Universal API

Secure video hosting and streaming APIs for uploading, managing, protecting, and playing back VdoCipher videos.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/vdoCipher/latest
- **Category:** Content & Files / Storage
- **Actions:** 26
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.vdocipher.com/
- **Vendor API docs:** https://www.vdocipher.com/page/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Videos](actions/list-videos.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vdoCipher/latest/actions/list-videos?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (26)

### Chapter

| Action | Method | Description |
| --- | --- | --- |
| [Get Video Chapters](actions/get-video-chapters.md) | GET | Retrieves video chapters from VdoCipher. |
| [Update Video Chapters](actions/update-video-chapters.md) | PUT | Updates video chapters in VdoCipher. |

### Playback Otp

| Action | Method | Description |
| --- | --- | --- |
| [Create Video OTP](actions/create-video-otp.md) | POST | Creates a playback OTP in VdoCipher. |

### Policy

| Action | Method | Description |
| --- | --- | --- |
| [Create Policy](actions/create-policy.md) | POST | Creates a new policy in VdoCipher. |
| [Delete Policy](actions/delete-policy.md) | DELETE | Deletes an existing policy from VdoCipher. |
| [List Policies](actions/list-policies.md) | GET | Lists policies in VdoCipher. |
| [Update Policy](actions/update-policy.md) | PUT | Updates an existing policy in VdoCipher. |

### Video

| Action | Method | Description |
| --- | --- | --- |
| [Delete Video](actions/delete-video.md) | DELETE | Deletes an existing video from VdoCipher. |
| [Get Video](actions/get-video.md) | GET | Retrieves video details from VdoCipher. |
| [Import Video URL](actions/import-video-url.md) | POST | Imports a video from a URL into VdoCipher. |
| [List Videos](actions/list-videos.md) | GET | Lists videos in VdoCipher. |
| [Update Video](actions/update-video.md) | PUT | Updates an existing video in VdoCipher. |

### Video File

| Action | Method | Description |
| --- | --- | --- |
| [Delete Video File](actions/delete-video-file.md) | DELETE | Deletes an existing video file from VdoCipher. |
| [Get Video File Download Url](actions/get-video-file-download-url.md) | GET | Retrieves a video file download URL from VdoCipher. |
| [List Video Files](actions/list-video-files.md) | GET | Lists video files in VdoCipher. |
| [Upload Video File](actions/upload-video-file.md) | POST | Uploads a poster or subtitle file to VdoCipher. |

### Video Parameter

| Action | Method | Description |
| --- | --- | --- |
| [Get Video Parameters](actions/get-video-parameters.md) | GET | Retrieves video parameters from VdoCipher. |
| [Update Video Parameters](actions/update-video-parameters.md) | PUT | Updates video parameters in VdoCipher. |

### Video Tag

| Action | Method | Description |
| --- | --- | --- |
| [Add Video Tags](actions/add-video-tags.md) | PUT | Adds tags to videos in VdoCipher. |
| [List Video Tags](actions/list-video-tags.md) | GET | Lists video tags in VdoCipher. |
| [Set Video Tags](actions/set-video-tags.md) | PUT | Replaces video tags for a VdoCipher video. |

### Video Upload

| Action | Method | Description |
| --- | --- | --- |
| [Create Video Upload Policy](actions/create-video-upload-policy.md) | GET | Retrieves an upload policy for a new VdoCipher video. |
| [Replace Video Upload Policy](actions/replace-video-upload-policy.md) | GET | Retrieves an upload policy for replacing a VdoCipher video. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in VdoCipher. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from VdoCipher. |
| [List Webhooks](actions/list-webhooks.md) | GET | Lists webhooks in VdoCipher. |

