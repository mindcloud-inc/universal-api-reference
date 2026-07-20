# Upload File with Amberscript

Uploads a file to create an Amberscript job.

## Endpoint

- **Method:** `POST`
- **Path:** `/jobs/upload-media`
- **Base URL:** `https://api.amberscript.com/api`
- **Official documentation:** [Upload File](https://amberscript.github.io/api-docs/#uploading-a-file)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Audio or video file to upload. |
| `language` | query | `string` | no | Language code for the uploaded media. Use `auto` to let Amberscript detect supported languages automatically. |
| `transcriptionType` | query | `string` | no | `transcription`, `captions`, or `translatedSubtitles`. |
| `jobType` | query | `string` | no | `direct` for automatic jobs or `perfect` for manual jobs. |
| `numberOfSpeakers` | query | `number` | no | Known speaker count from `0` to `5`. |
| `callbackUrl` | query | `string` | no | Optional webhook URL for final job status callbacks. |
| `glossaryId` | query | `string` | no | Optional glossary to apply to this upload. |
| `transcriptionStyle` | query | `string` | no | Transcript style: `cleanread` or `verbatim`. |
| `turnaroundTime` | query | `string` | no | Optional turnaround time for manual jobs. |
| `targetLanguage` | query | `string` | no | Target language code when requesting translated subtitles during upload. |
