# Add Number Group Members with CallScaler

Updates a number group in CallScaler by adding members.

## Endpoint

- **Method:** `POST`
- **Path:** `/number-groups/:id/members`
- **Base URL:** `https://callscaler.com/api/v1`
- **Official documentation:** [Add Number Group Members](https://callscaler.com/docs/api-resources)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `number_ids[]` | body | `array<string>` | no | Numbers to add to the group. Send multiple values as a array. |
