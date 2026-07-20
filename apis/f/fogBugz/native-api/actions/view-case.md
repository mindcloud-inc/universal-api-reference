# View Case with FogBugz

Retrieves case details from FogBugz.

## Endpoint

- **Method:** `POST`
- **Path:** `/viewCase`
- **Base URL:** `{siteUrl}/api`
- **Official documentation:** [View Case](https://support.fogbugz.com/article/55722-frequently-used-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ixBug` | body | `number` | yes | The case you want to view. |
