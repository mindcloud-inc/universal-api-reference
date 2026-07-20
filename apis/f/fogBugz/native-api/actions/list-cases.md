# List Cases with FogBugz

Retrieves cases from FogBugz.

## Endpoint

- **Method:** `POST`
- **Path:** `/listCases`
- **Base URL:** `{siteUrl}/api`
- **Official documentation:** [List Cases](https://support.fogbugz.com/article/55766-fogbugz-api-listing-searching-and-viewing-cases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sFilter` | body | `string` | no | Show only cases returned by a specific saved filter. |
| `max` | body | `number` | no | Maximum number of cases to return. |
