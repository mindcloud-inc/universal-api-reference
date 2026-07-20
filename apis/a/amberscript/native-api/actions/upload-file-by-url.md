# Upload File by URL with Amberscript

Uploads a file URL to create an Amberscript job.

## Endpoint

- **Method:** `POST`
- **Path:** `/jobs/upload-media-from-url`
- **Base URL:** `https://api.amberscript.com/api`
- **Official documentation:** [Upload File by URL](https://amberscript.github.io/api-docs/#uploading-a-file-by-url)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sourceUrl` | body | `string` | yes | Publicly accessible or presigned media URL. |
| `language` | body | `string` | no | Language code for the media. Use `auto` to let Amberscript detect supported languages automatically. |
| `transcriptionType` | body | `string` | no | `transcription`, `captions`, or `translatedSubtitles`. |
| `jobType` | body | `string` | no | `direct` for automatic jobs or `perfect` for manual jobs. |
| `numberOfSpeakers` | body | `number` | no | Known speaker count from `0` to `5`. |
| `callbackUrl` | body | `string` | no | Optional webhook URL for final job status callbacks. |
| `glossaryId` | body | `string` | no | Optional glossary to apply to this upload. |
| `transcriptionStyle` | body | `string` | no | Transcript style: `cleanread` or `verbatim`. |
| `turnaroundTime` | body | `string` | no | Optional turnaround time for manual jobs. |
| `targetLanguage` | body | `string` | no | Target language code when requesting translated subtitles. |
