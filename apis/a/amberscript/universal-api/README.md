# <img src="https://images.mindcloud.co/apps/icons/amberscript_1775570834129.png" alt="Amberscript logo" width="28" height="28"> Amberscript: Universal API

Upload media, track transcription jobs, and manage glossaries

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/amberscript/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.amberscript.com
- **Vendor API docs:** https://amberscript.github.io/api-docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Jobs](actions/list-jobs.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amberscript/latest/actions/list-jobs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Glossary

| Action | Method | Description |
| --- | --- | --- |
| [Create Glossary](actions/create-glossary.md) | POST | Creates a new glossary in Amberscript. |
| [Delete Glossary](actions/delete-glossary.md) | DELETE | Deletes an existing glossary from Amberscript. |
| [List Glossaries](actions/list-glossaries.md) | GET | Retrieves glossaries from your Amberscript account. |
| [Update Glossary](actions/update-glossary.md) | PUT | Updates an existing glossary in Amberscript. |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Delete Job](actions/delete-job.md) | DELETE | Deletes an existing job from Amberscript. |
| [Get Job Status](actions/get-job-status.md) | GET | Retrieves the status of an Amberscript job. |
| [List Jobs](actions/list-jobs.md) | GET | Retrieves jobs from your Amberscript account. |
| [Request Translated Subtitles](actions/request-translated-subtitles.md) | POST | Requests translated subtitles for an existing Amberscript manual captions job. |
| [Upload File](actions/upload-file.md) | POST | Uploads a file to create an Amberscript job. |
| [Upload File by URL](actions/upload-file-by-url.md) | POST | Uploads a file URL to create an Amberscript job. |

### Job Export

| Action | Method | Description |
| --- | --- | --- |
| [Export JSON](actions/export-json.md) | GET | Retrieves JSON export for an Amberscript job. |
| [Export SRT](actions/export-srt.md) | GET | Retrieves SRT subtitle export for an Amberscript job. |
| [Export STL](actions/export-stl.md) | GET | Retrieves STL subtitle export for an Amberscript job. |
| [Export TXT](actions/export-txt.md) | GET | Retrieves plain text export for an Amberscript job. |
| [Export VTT](actions/export-vtt.md) | GET | Retrieves VTT subtitle export for an Amberscript job. |

