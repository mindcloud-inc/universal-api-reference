# Update User Settings with Leadberry

## Endpoint

- **Method:** `POST`
- **Path:** `/data/changeUserSettings`
- **Base URL:** `https://app.leadberry.com`
- **Official documentation:** [Update User Settings](https://app.leadberry.com/js/dist/all.min.js?ver=20221103_1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `string` | no | Leadberry setting change type, such as email, pay2goChargeAuto, filterSensitivity, or toggleProfile. |
| `value` | body | `string` | no | Setting value payload associated with the type. |
