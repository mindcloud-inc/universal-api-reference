# Update Form General Settings with Global Patron

Updates form general settings in Global Patron.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/restricted/form/{formId}/?updateSettingsOnly=1&settingsSection=generalsettings`
- **Base URL:** `https://api.globalpatron.com`
- **Official documentation:** [Update Form General Settings](https://www.globalpatron.com/developers/api/forms/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | ID of the form to update. |
