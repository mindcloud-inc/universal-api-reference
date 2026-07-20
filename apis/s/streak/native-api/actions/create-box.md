# Create Box with Streak

Creates a new box in Streak.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/pipelines/:pipelineKey/boxes`
- **Base URL:** `https://api.streak.com`
- **Official documentation:** [Create Box](https://streak.readme.io/reference/create-a-box)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pipelineKey` | path | `list<string>` | yes | The key of the pipeline the box should belong to. |
| `name` | body | `string` | yes | The name of this box. |
| `stageKey` | body | `string` | no | The stage of this box. |
| `notes` | body | `string` | no | The notes on the box. |
| `assignedToSharingEntries` | body | `string` | no | The member(s) of your team this box will be assigned to. This must be an array of objects with `email` properties encoded as a JSON string. |
