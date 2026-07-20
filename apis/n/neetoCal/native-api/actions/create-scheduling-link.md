# Create Scheduling Link with NeetoCal

Creates a new scheduling link in NeetoCal.

## Endpoint

- **Method:** `POST`
- **Path:** `/meetings`
- **Base URL:** `https://{subdomain}.neetocal.com/api/external/v2`
- **Official documentation:** [Create Scheduling Link](https://apidocs.neetocal.com/api-reference/scheduling-links/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | body | `string` | yes | Unique slug for the scheduling link. |
| `name` | body | `string` | yes | Display name for the scheduling link. |
| `hosts[]` | body | `array<string>` | yes | Host emails for the scheduling link. |
| `duration` | body | `number` | yes | Duration in minutes. |
