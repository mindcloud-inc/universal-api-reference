# Create List with Campaign Monitor

Creates a new list in Campaign Monitor.

## Endpoint

- **Method:** `POST`
- **Path:** `/lists/:clientId.json`
- **Base URL:** `https://api.createsend.com/api/v3.3`
- **Official documentation:** [Create List](https://www.campaignmonitor.com/api/v3-3/lists/#creating-a-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `clientId` | path | `string` | yes | Campaign Monitor client identifier. |
| `Title` | body | `string` | yes | Title of the list. |
| `UnsubscribePage` | body | `string` | no | URL for the list unsubscribe page. |
| `ConfirmedOptIn` | body | `boolean` | no | Whether the list requires confirmed opt-in. |
| `ConfirmationSuccessPage` | body | `string` | no | URL used after confirmation succeeds. |
| `UnsubscribeSetting` | body | `string` | no | Campaign Monitor unsubscribe behavior for the list. |
