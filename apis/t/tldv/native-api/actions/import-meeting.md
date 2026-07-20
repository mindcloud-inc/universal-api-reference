# Import Meeting with tl:dv

Imports a meeting into tl:dv from a URL.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1alpha1/meetings/import`
- **Base URL:** `https://pasta.tldv.io`
- **Official documentation:** [Import Meeting](https://doc.tldv.io/index.html#tag/Meetings/operation/ImportController.ImportMeeting)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of the meeting or recording being imported. |
| `url` | body | `string` | yes | The public URL of the meeting or recording to import. |
| `happenedAt` | body | `date` | no | The meeting or recording date and time. |
| `dryRun` | body | `boolean` | no | Run the import as a dry run without persisting it. |
| `participants[]` | body | `array<string>` | no | Invitee email addresses for the imported meeting. |
