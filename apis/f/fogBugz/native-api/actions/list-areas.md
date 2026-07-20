# List Areas with FogBugz

Retrieves areas from FogBugz.

## Endpoint

- **Method:** `POST`
- **Path:** `/listAreas`
- **Base URL:** `{siteUrl}/api`
- **Official documentation:** [List Areas](https://support.fogbugz.com/en-us/article/55768-fogbugz-xml-api-lists)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fWrite` | body | `boolean` | no | Set to true to include only areas you can modify. |
| `ixProject` | body | `number` | no | Limit results to areas in a specific project. |
| `ixArea` | body | `number` | no | Include a specific area even if it is deleted. |
