# List Organizations with Zeplin

Retrieves a list of organizations from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [List Organizations](https://docs.zeplin.dev/reference/getorganizations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `role[]` | query | `array<string>` | no | Filter by role ☝️Note that the Developer role maps to `member` and the Reviewer role maps to `alien` in the API. Example: `?role=owner&role=admin` |
