# Get or Create Organization with Streak

Finds an organization in Streak, or creates one if needed.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/teams/:teamKey/organizations`
- **Base URL:** `https://api.streak.com`
- **Official documentation:** [Get or Create Organization](https://streak.readme.io/reference/create-an-organization)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `teamKey` | path | `string` | yes |
| `domains[]` | body | `array<string>` | yes |
