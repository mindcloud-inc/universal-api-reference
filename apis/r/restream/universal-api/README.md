# <img src="https://images.mindcloud.co/apps/icons/images-6_1775763479556.jpeg" alt="Restream logo" width="28" height="28"> Restream: Universal API

Restream API for profiles, channels, events, recordings, storage, clips, and studio resources.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/restream/latest
- **Category:** Communication / Video Communications
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://restream.io
- **Vendor API docs:** https://developers.restream.io

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Profile](actions/get-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/restream/latest/actions/get-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [List Studio Brands](actions/list-studio-brands.md) | GET | Retrieves studio brands from Restream. |
| [List Studio Captions](actions/list-studio-captions.md) | GET | Retrieves studio captions from Restream. |
| [List Studio QR Codes](actions/list-studio-qr-codes.md) | GET | Retrieves studio QR codes from Restream. |
| [Update Studio Caption](actions/update-studio-caption.md) | PUT | Updates a studio caption in Restream. |
| [Update Studio QR Code](actions/update-studio-qr-code.md) | PUT | Updates a studio QR code in Restream. |

### Channels

| Action | Method | Description |
| --- | --- | --- |
| [Add Channel](actions/add-channel.md) | POST | Creates a streaming channel in Restream. |
| [Delete Channel](actions/delete-channel.md) | DELETE | Deletes a streaming channel from Restream. |
| [Get Channel](actions/get-channel.md) | GET | Retrieves a streaming channel from Restream by ID. |
| [List Channels](actions/list-channels.md) | GET | Retrieves connected streaming channels from Restream. |

### Connections

| Action | Method | Description |
| --- | --- | --- |
| [Get Stream Key](actions/get-stream-key.md) | GET | Retrieves the authenticated user stream key from Restream. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Get Event](actions/get-event.md) | GET | Retrieves an event from Restream by ID. |
| [Get Event Stream Key](actions/get-event-stream-key.md) | GET | Retrieves an event stream key from Restream. |
| [List Events History](actions/list-events-history.md) | GET | Retrieves past events from Restream. |
| [List In Progress Events](actions/list-in-progress-events.md) | GET | Retrieves in-progress events from Restream. |
| [List Upcoming Events](actions/list-upcoming-events.md) | GET | Retrieves upcoming events from Restream. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Create Event Recording Download URL](actions/create-event-recording-download-url.md) | GET | Generates a download URL for an event recording in Restream. |
| [Create Storage File Download URL](actions/create-storage-file-download-url.md) | GET | Generates a download URL for a storage file in Restream. |
| [Get Clip Download URL](actions/get-clip-download-url.md) | GET | Generates a download URL for a clip in Restream. |
| [Get Storage File](actions/get-storage-file.md) | GET | Retrieves a video storage file from Restream. |
| [List Event Recordings](actions/list-event-recordings.md) | GET | Retrieves event recordings from Restream. |
| [List Storage Files](actions/list-storage-files.md) | GET | Retrieves video storage files from Restream. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Get Clip Project](actions/get-clip-project.md) | GET | Retrieves a clip project from Restream by ID. |
| [List Clip Projects](actions/list-clip-projects.md) | GET | Retrieves clip projects from Restream. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Profile](actions/get-profile.md) | GET | Retrieves the authenticated user profile from Restream. |

