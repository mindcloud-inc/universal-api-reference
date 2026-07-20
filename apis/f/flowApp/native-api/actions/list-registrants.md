# List Registrants with Flow App

## Endpoint

- **Method:** `GET`
- **Path:** `/reports/events/sessions/registrants/:sessionToken`
- **Base URL:** `https://prod.flowapp.com/api/v1`
- **Official documentation:** [List Registrants](https://support.flowapp.com/support/solutions/articles/12000076814-flow-api-0-0-4)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionToken` | path | `string` | yes | The event session token whose registrants you want to list. |
