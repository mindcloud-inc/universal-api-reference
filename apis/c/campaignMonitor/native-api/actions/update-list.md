# Update List with Campaign Monitor

Updates an existing list in Campaign Monitor.

## Endpoint

- **Method:** `PUT`
- **Path:** `/lists/:listId.json`
- **Base URL:** `https://api.createsend.com/api/v3.3`
- **Official documentation:** [Update List](https://www.campaignmonitor.com/api/v3-3/lists/#updating-a-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | path | `string` | yes | Campaign Monitor list identifier. |
| `Title` | body | `string` | no | Title of the list. |
| `UnsubscribePage` | body | `string` | no | URL for the list unsubscribe page. |
| `ConfirmedOptIn` | body | `boolean` | no | Whether the list requires confirmed opt-in. |
| `ConfirmationSuccessPage` | body | `string` | no | URL used after confirmation succeeds. |
| `UnsubscribeSetting` | body | `string` | no | Campaign Monitor unsubscribe behavior for the list. |
