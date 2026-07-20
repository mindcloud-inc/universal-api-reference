# Update Numeric Variable with Apilio

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/numeric_variables/{{uuid}}`
- **Base URL:** `https://api.apilio.com`
- **Official documentation:** [Update Numeric Variable](https://documenter.getpostman.com/view/13480928/TzCHAVD2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `numeric_variable.value` | body | `number` | yes | The new numeric value for the numeric variable. |
| `uuid` | path | `string` | yes | The UUID of the numeric variable to update. |
