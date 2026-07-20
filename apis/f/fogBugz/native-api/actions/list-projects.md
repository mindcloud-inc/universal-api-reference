# List Projects with FogBugz

Retrieves projects from FogBugz.

## Endpoint

- **Method:** `POST`
- **Path:** `/listProjects`
- **Base URL:** `{siteUrl}/api`
- **Official documentation:** [List Projects](https://support.fogbugz.com/en-us/article/55768-fogbugz-xml-api-lists)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fWrite` | body | `boolean` | no | Set to true to include only projects you can modify. |
| `ixProject` | body | `number` | no | Include a specific project even if it is deleted. |
| `fDeleted` | body | `boolean` | no | Set to true to include deleted projects. |
