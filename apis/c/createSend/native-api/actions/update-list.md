# Update List with CreateSend

Updates an existing list in CreateSend.

## Endpoint

- **Method:** `PUT`
- **Path:** `/lists/:listId.json`
- **Base URL:** `https://api.createsend.com/api/v3.3`
- **Official documentation:** [Update List](https://www.campaignmonitor.com/api/lists/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `listId` | path | `string` | yes |
| `Title` | body | `string` | no |
| `UnsubscribePage` | body | `string` | no |
| `ConfirmedOptIn` | body | `boolean` | no |
| `ConfirmationSuccessPage` | body | `string` | no |
| `UnsubscribeSetting` | body | `string` | no |
