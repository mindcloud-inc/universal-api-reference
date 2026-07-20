# Start Widget Call with CallPage

Starts a widget call in CallPage.

## Endpoint

- **Method:** `POST`
- **Path:** `/widgets/call`
- **Base URL:** `https://core.callpage.io/api/v1/external`
- **Official documentation:** [Start Widget Call](https://callpage.github.io/documentation-rest/#simple-call)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `number` | yes | Widget identifier. |
| `tel` | body | `string` | yes | Phone number to call in E.164 format. |
| `department_id` | body | `number` | no | Optional department identifier. |
| `manager_id` | body | `number` | no | Optional manager identifier. |
