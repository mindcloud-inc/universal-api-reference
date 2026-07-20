# V3 Create Mention with Timeular

Creates a new mention in the Timeular v3 API.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v3/mentions`
- **Base URL:** `https://api.early.app`
- **Official documentation:** [V3 Create Mention](https://developers.early.app/#b0de30da-39f4-4d21-b5d5-09e79940c820)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `key` | body | `string` | yes |
| `label` | body | `string` | yes |
| `scope` | body | `string` | yes |
| `spaceId` | body | `string` | no |
