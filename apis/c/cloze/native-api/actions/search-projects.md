# Search Projects with Cloze

Finds projects in Cloze.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/find`
- **Base URL:** `https://api.cloze.com`
- **Official documentation:** [Search Projects](https://api.cloze.com/api-docs/#/paths/v1-projects-find/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assignee` | query | `string` | no | Email of the assignee. |
| `freeformquery` | query | `string` | no | Natural language query expression. |
| `pagenumber` | query | `number` | no | Page number to retrieve starting from 1. |
| `segment` | query | `string` | no | Project segment selector. |
| `stage` | query | `string` | no | Project stage selector. |
| `step` | query | `string` | no | Next step unique id selector. |
| `countonly` | query | `boolean` | no | Return only the available count. |
| `sort` | query | `string` | no | Sort order. Accepted values: `0`, `1`, `10`, `11`, `12`, `13`, `14`, `15`, `16`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. |
| `group` | query | `string` | no | Group order. Accepted values: `0`, `1`. |
| `assigned` | query | `boolean` | no | Whether the project is assigned. |
