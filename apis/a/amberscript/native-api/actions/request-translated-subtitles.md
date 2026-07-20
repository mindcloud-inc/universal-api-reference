# Request Translated Subtitles with Amberscript

Requests translated subtitles for an existing Amberscript manual captions job.

## Endpoint

- **Method:** `POST`
- **Path:** `/jobs/translatedSubtitles`
- **Base URL:** `https://api.amberscript.com/api`
- **Official documentation:** [Request Translated Subtitles](https://amberscript.github.io/api-docs/#request-translated-subtitles-for-an-existing-manual-39-perfect-39-captions-job)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sourceJobId` | query | `string` | yes | Existing manual captions job to translate. |
| `targetLanguage` | query | `string` | yes | Target language code for the translated subtitles job. |
| `turnaroundTime` | query | `string` | no | Optional turnaround time for the translated subtitles job. |
| `callbackUrl` | query | `string` | no | Optional webhook URL for final job status callbacks. |
| `notes` | query | `string` | no | Optional notes for the translated subtitles job. |
