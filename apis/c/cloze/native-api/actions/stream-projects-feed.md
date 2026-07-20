# Stream Projects Feed with Cloze

Retrieves the projects feed from Cloze.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/feed`
- **Base URL:** `https://api.cloze.com`
- **Official documentation:** [Stream Projects Feed](https://api.cloze.com/api-docs/#/paths/v1-projects-feed/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cursor` | query | `string` | no | Cursor to the next batch of results from the previous feed response. |
| `freeformquery` | query | `string` | no | Natural language query expression. |
| `modifiedafter` | query | `string` | no | Starting point in UTC milliseconds for change polling. |
| `scope` | query | `string` | no | Project scope selector. |
| `segment` | query | `string` | no | Project segment selector. |
| `stage` | query | `string` | no | Project stage selector. |
| `keysonly` | query | `boolean` | no | Return just the syncKey field. |
| `includeauditedchanges` | query | `boolean` | no | Include audited changes in feed results. |
