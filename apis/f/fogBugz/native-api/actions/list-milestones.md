# List Milestones with FogBugz

Retrieves milestones from FogBugz.

## Endpoint

- **Method:** `POST`
- **Path:** `/listFixFors`
- **Base URL:** `{siteUrl}/api`
- **Official documentation:** [List Milestones](https://support.fogbugz.com/en-us/article/55768-fogbugz-xml-api-lists)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ixProject` | body | `number` | no | Show milestones for a specific project. |
| `ixFixFor` | body | `number` | no | Include a specific milestone even if it is unassignable. |
| `fIncludeDeleted` | body | `boolean` | no | Set to true to include unassignable milestones. |
| `fIncludeReallyDeleted` | body | `boolean` | no | Set to true to include deleted milestones. |
