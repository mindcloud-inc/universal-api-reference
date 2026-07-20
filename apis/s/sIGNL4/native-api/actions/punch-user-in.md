# Punch User In with SIGNL4

Updates a user's duty status to on-duty in SIGNL4.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/duties/punchIn`
- **Base URL:** `https://connect.signl4.com/api`
- **Official documentation:** [Punch User In](https://connect.signl4.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `userId` | body | `string` | yes |
| `teamIds[]` | body | `array<string>` | no |
