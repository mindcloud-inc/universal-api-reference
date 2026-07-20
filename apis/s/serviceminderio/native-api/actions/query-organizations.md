# Query Organizations with serviceminder.io

Finds organizations in ServiceMinder by name.

## Endpoint

- **Method:** `POST`
- **Path:** `/organizations/query`
- **Base URL:** `https://serviceminder.com/api`
- **Official documentation:** [Query Organizations](https://serviceminder.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `NameSearch` | body | `string` | no | Search organizations by name. |
