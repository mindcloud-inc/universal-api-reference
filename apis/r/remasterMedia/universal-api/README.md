# <img src="https://images.mindcloud.co/apps/icons/remastermedia-icon_1776711765300.png" alt="RemasterMedia logo" width="28" height="28"> RemasterMedia: Universal API

RemasterMedia is an audio and video sound-processing API for uploading media, applying remastering and noise-reduction actions, generating derived media assets, and retrieving mediafile details and presets.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/remasterMedia/latest
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.remastermedia.com
- **Vendor API docs:** https://www.remastermedia.com/developers

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Mediafile](actions/get-mediafile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/remasterMedia/latest/actions/get-mediafile?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Auth Token

| Action | Method | Description |
| --- | --- | --- |
| [Authenticate](actions/authenticate.md) | POST | Creates an auth token in RemasterMedia. |

### Denoise Preset

| Action | Method | Description |
| --- | --- | --- |
| [List Denoise Presets](actions/list-denoise-presets.md) | GET | Retrieves noise reduction presets from RemasterMedia. |

### Mediafile

| Action | Method | Description |
| --- | --- | --- |
| [Create Mediafile](actions/create-mediafile.md) | POST | Creates a mediafile in RemasterMedia. |
| [Create Poster](actions/create-poster.md) | POST | Creates a poster mediafile in RemasterMedia. |
| [Create Remaster](actions/create-remaster.md) | POST | Creates a remastered mediafile in RemasterMedia. |
| [Create Waveform](actions/create-waveform.md) | POST | Creates a waveform mediafile in RemasterMedia. |
| [Denoise Mediafile](actions/denoise-mediafile.md) | POST | Creates a denoised mediafile in RemasterMedia using a preset. |
| [Denoise Mediafile With Parameters](actions/denoise-mediafile-with-parameters.md) | POST | Creates a denoised mediafile in RemasterMedia using direct parameters. |
| [Get Mediafile](actions/get-mediafile.md) | GET | Retrieves mediafile details from RemasterMedia. |
| [Get Source Mediafile](actions/get-source-mediafile.md) | GET | Retrieves the source mediafile from RemasterMedia. |
| [List Derived Mediafiles](actions/list-derived-mediafiles.md) | GET | Retrieves derived mediafiles from RemasterMedia. |
| [List Mediafiles](actions/list-mediafiles.md) | GET | Retrieves mediafiles from RemasterMedia. |
| [Process Mediafile](actions/process-mediafile.md) | POST | Processes a mediafile in RemasterMedia with action-specific options. |

### Remastering Preset

| Action | Method | Description |
| --- | --- | --- |
| [List Remastering Presets](actions/list-remastering-presets.md) | GET | Retrieves remastering presets from RemasterMedia. |

