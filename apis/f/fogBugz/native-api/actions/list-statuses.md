# List Statuses with FogBugz

Retrieves statuses from FogBugz.

## Endpoint

- **Method:** `POST`
- **Path:** `/listStatuses`
- **Base URL:** `{siteUrl}/api`
- **Official documentation:** [List Statuses](https://support.fogbugz.com/en-us/article/55768-fogbugz-xml-api-lists)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ixCategory` | body | `number` | no | Return statuses for a specific category. |
| `fResolved` | body | `boolean` | no | Set to true to return only resolved statuses. |
