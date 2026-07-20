# List People with FogBugz

Retrieves people from FogBugz.

## Endpoint

- **Method:** `POST`
- **Path:** `/listPeople`
- **Base URL:** `{siteUrl}/api`
- **Official documentation:** [List People](https://support.fogbugz.com/en-us/article/55768-fogbugz-xml-api-lists)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fIncludeActive` | body | `boolean` | no | Set to true to include active users. |
| `fIncludeNormal` | body | `boolean` | no | Set to true to include normal users. |
| `fIncludeDeleted` | body | `boolean` | no | Set to true to include deleted users. |
| `fIncludeCommunity` | body | `boolean` | no | Set to true to include community users. |
| `fIncludeVirtual` | body | `boolean` | no | Set to true to include virtual users. |
