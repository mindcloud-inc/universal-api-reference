# Add Content Record with Cloze

Creates a content record in Cloze.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/timeline/content/create`
- **Base URL:** `https://api.cloze.com`
- **Official documentation:** [Add Content Record](https://api.cloze.com/api-docs/#/paths/v1-timeline-content-create/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `style` | body | `string` | no | Style of the content record. Accepted values: `0`, `1`, `2`, `3`. |
| `from` | body | `string` | no | Address of the person who created the content record. |
| `uniqueid` | body | `string` | no | Unique identifier for the content record. |
| `source` | body | `string` | no | Source domain for the content record. |
| `subject` | body | `string` | no | Subject of the content record. |
| `body` | body | `string` | no | Body text of the content record. |
