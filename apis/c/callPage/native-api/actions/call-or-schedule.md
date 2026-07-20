# Call Or Schedule with CallPage

Starts or schedules a widget call in CallPage.

## Endpoint

- **Method:** `POST`
- **Path:** `/widgets/call-or-schedule`
- **Base URL:** `https://core.callpage.io/api/v1/external`
- **Official documentation:** [Call Or Schedule](https://callpage.github.io/documentation-rest/#call-or-schedule)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `number` | yes | Widget identifier. |
| `tel` | body | `string` | yes | Phone number to call in E.164 format. |
| `department_id` | body | `number` | no | Optional department identifier. |
