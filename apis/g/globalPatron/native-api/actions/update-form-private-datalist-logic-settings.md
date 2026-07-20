# Update Form Private Datalist Logic Settings with Global Patron

Updates form private datalist logic settings in Global Patron.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/restricted/form/{formId}/?updateSettingsOnly=1&settingsSection=privatedatalistlogicsettings`
- **Base URL:** `https://api.globalpatron.com`
- **Official documentation:** [Update Form Private Datalist Logic Settings](https://www.globalpatron.com/developers/api/forms/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | ID of the form to update. |
