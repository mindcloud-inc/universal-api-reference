# List Projects with Paymo

Retrieves projects from Paymo.

## Endpoint

- **Method:** `GET`
- **Path:** `projects`
- **Base URL:** `https://app.paymoapp.com/api/`
- **Official documentation:** [List Projects](https://github.com/paymo-org/api/blob/master/sections/projects.md#getting-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `where` | query | `string` | no | Optional raw Paymo filtering expression, for example `client_id=1295766 and active=true`. |
