# Delete Form with Global Patron

Deletes a form from Global Patron.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/restricted/form/{formId}/?updateSettingsOnly=1&settingsSection=generalsettingsdelete`
- **Base URL:** `https://api.globalpatron.com`
- **Official documentation:** [Delete Form](https://www.globalpatron.com/developers/api/forms/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | ID of the form to delete. |
