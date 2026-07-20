# Update Form Conditional Logic Settings with Global Patron

Updates form conditional logic settings in Global Patron.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/restricted/form/{formId}/?updateSettingsOnly=1&settingsSection=conditionallogicsettings`
- **Base URL:** `https://api.globalpatron.com`
- **Official documentation:** [Update Form Conditional Logic Settings](https://www.globalpatron.com/developers/api/forms/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | ID of the form to update. |
