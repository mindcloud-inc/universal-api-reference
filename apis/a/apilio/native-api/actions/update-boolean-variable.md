# Update Boolean Variable with Apilio

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/boolean_variables/{{uuid}}`
- **Base URL:** `https://api.apilio.com`
- **Official documentation:** [Update Boolean Variable](https://documenter.getpostman.com/view/13480928/TzCHAVD2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `boolean_variable.value` | body | `boolean` | yes | The new boolean value for the boolean variable. |
| `uuid` | path | `string` | yes | The UUID of the boolean variable to update. |
