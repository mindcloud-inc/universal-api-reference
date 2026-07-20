# Create List with CreateSend

Creates a new list in CreateSend.

## Endpoint

- **Method:** `POST`
- **Path:** `/lists/:clientId.json`
- **Base URL:** `https://api.createsend.com/api/v3.3`
- **Official documentation:** [Create List](https://www.campaignmonitor.com/api/lists/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `clientId` | path | `string` | yes |
| `Title` | body | `string` | yes |
| `UnsubscribePage` | body | `string` | no |
| `ConfirmedOptIn` | body | `boolean` | no |
| `ConfirmationSuccessPage` | body | `string` | no |
| `UnsubscribeSetting` | body | `string` | no |
