# Stream Companies Feed with Cloze

Retrieves the companies feed from Cloze.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/companies/feed`
- **Base URL:** `https://api.cloze.com`
- **Official documentation:** [Stream Companies Feed](https://api.cloze.com/api-docs/#/paths/v1-companies-feed/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cursor` | query | `string` | no | Cursor returned by the previous feed response. |
| `freeformquery` | query | `string` | no | Natural-language or UI-style Cloze query expression on the initial request. |
| `includeauditedchanges` | query | `boolean` | no | Return change audit details in results for each delivered company. |
| `keysonly` | query | `boolean` | no | Return only the syncKey field for each record. |
| `modifiedafter` | query | `string` | no | UTC milliseconds or now. Set on the initial request to control the feed starting point. |
| `pagesize` | query | `number` | no | Limit results per batch. Set on the initial request. |
| `scope` | query | `string` | no | Scope of matching relations. Set on the initial request. |
| `segment` | query | `string` | no | Filter by segment on the initial request. |
| `stage` | query | `list<string>` | no | Filter by stage on the initial request. Accepted values: `current`, `future`, `lead`, `out`, `past`. |
