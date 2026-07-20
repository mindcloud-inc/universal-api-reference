# Search Companies with Cloze

Finds companies in Cloze.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/companies/find`
- **Base URL:** `https://api.cloze.com`
- **Official documentation:** [Search Companies](https://api.cloze.com/api-docs/#/paths/v1-companies-find/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assigned` | query | `boolean` | no | Filter by whether the company is assigned. |
| `assignee` | query | `string` | no | Filter by assignee email when assigned is true. |
| `countonly` | query | `boolean` | no | Return only the available count without company records. |
| `freeformquery` | query | `string` | no | Natural-language or UI-style Cloze query expression. |
| `group` | query | `list<string>` | no | Group order for matching companies. Accepted values: `stage`, `subteam`. |
| `pagenumber` | query | `number` | no | Page number to retrieve, starting from 1. |
| `pagesize` | query | `number` | no | Limit results per page. Default 10, maximum 1000. |
| `scope` | query | `string` | no | Scope of matching relations, such as local or team. Set on the initial request. |
| `segment` | query | `string` | no | Filter by segment id or current segment name. |
| `sort` | query | `list<string>` | no | Sort order for matching companies. Accepted values: `assigned`, `bestrelationship`, `created`, `distance`, `duenext`, `duepast`, `end`, `first`, `firstmet`, `last`, `lastchanged`, `lasttalked`, `name`, `nextstep`, `start`, `value`, `wentquiet`. |
| `stage` | query | `list<string>` | no | Filter by company stage. Accepted values: `current`, `future`, `lead`, `out`, `past`. |
| `step` | query | `string` | no | Filter by next step unique id. |
