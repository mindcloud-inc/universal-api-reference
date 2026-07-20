# Update String Variable with Apilio

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/string_variables/{{uuid}}`
- **Base URL:** `https://api.apilio.com`
- **Official documentation:** [Update String Variable](https://documenter.getpostman.com/view/13480928/TzCHAVD2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `string_variable.value` | body | `string` | yes | The new string value for the string variable. |
| `uuid` | path | `string` | yes | The UUID of the string variable to update. |
