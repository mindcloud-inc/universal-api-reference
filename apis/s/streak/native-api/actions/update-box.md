# Update Box with Streak

Updates an existing box in Streak.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/boxes/:boxKey`
- **Base URL:** `https://api.streak.com`
- **Official documentation:** [Update Box](https://streak.readme.io/reference/edit-a-box)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `boxKey` | path | `string` | yes | The key of the box to update. |
| `name` | body | `string` | no | The new name of the box. |
| `notes` | body | `string` | no | The notes of the box. |
| `stageKey` | body | `string` | no | The stage key the box should be moved to. |
| `followerKeys[]` | body | `array<string>` | no | The user keys who should follow this box. |
| `linkedBoxKeys[]` | body | `array<string>` | no | The box keys to link to the current box. |
| `assignedToSharingEntries[]` | body | `array<object>` | no | Each object needs an `email` field set to the assignee email. Send an empty array to unassign the box. |
| `contacts[]` | body | `array<object>` | no | The full contact array to associate with the box. |
| `organizations[]` | body | `array<object>` | no | The full organization array to associate with the box. |
| `fields` | body | `string` | no | Field keys and corresponding values, for example `{ "1007": "String", "1039": 42 }`, encoded as a JSON string. |
