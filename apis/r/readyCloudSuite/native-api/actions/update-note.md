# Update Note with ReadyCloud Suite

Updates an existing note in ReadyCloud Suite.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v2/orgs/:orgPk/orders/:orderPk/notes/:notePk/`
- **Base URL:** `https://www.readycloud.com`
- **Official documentation:** [Update Note](https://www.readycloud.com/static/api-doc/v2/02-apireference-v2-07-notes.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `notePk` | path | `string` | yes | ReadyCloud note identifier. |
| `orderPk` | path | `string` | yes | ReadyCloud order identifier. |
| `orgPk` | path | `string` | yes | ReadyCloud organization identifier. |
