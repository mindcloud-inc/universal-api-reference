# Check Domain Availability with Dub

Checks domain availability in Dub.

## Endpoint

- **Method:** `GET`
- **Path:** `/domains/status`
- **Base URL:** `https://api.dub.co`
- **Official documentation:** [Check Domain Availability](https://dub.co/docs/api-reference/domains/check-availability)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domains[]` | query | `array<string>` | yes | One or more .link domains to check. |
