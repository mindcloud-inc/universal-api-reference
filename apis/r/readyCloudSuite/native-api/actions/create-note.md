# Create Note with ReadyCloud Suite

Creates a new note in ReadyCloud Suite.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/orgs/:orgPk/orders/:orderPk/notes/`
- **Base URL:** `https://www.readycloud.com`
- **Official documentation:** [Create Note](https://www.readycloud.com/static/api-doc/v2/02-apireference-v2-07-notes.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderPk` | path | `string` | yes | ReadyCloud order identifier. |
| `orgPk` | path | `string` | yes | ReadyCloud organization identifier. |
