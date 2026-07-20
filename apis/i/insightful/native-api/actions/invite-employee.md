# Invite Employee with Insightful

Invites a new employee to your Insightful account.

## Endpoint

- **Method:** `POST`
- **Path:** `/employee`
- **Base URL:** `https://app.insightful.io/api/v1`
- **Official documentation:** [Invite Employee](https://developers.insightful.io/#58c5ec14-20c1-4d31-bb79-61420e26ebd9)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The employee email address. |
| `name` | body | `string` | yes | The employee name. |
| `sharedSettingsId` | body | `string` | yes | The shared settings ID to apply to the employee. |
| `teamId` | body | `string` | yes | The team ID the employee belongs to. |
