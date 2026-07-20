# Add Target with Intruder

## Endpoint

- **Method:** `POST`
- **Path:** `/targets/`
- **Base URL:** `https://api.intruder.io/v1`
- **Official documentation:** [Add Target](https://developers.intruder.io/reference/targets_create-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | body | `string` | yes | Target address or CIDR. |
| `tags[]` | body | `array<string>` | no | Tag names to add to the target. |
