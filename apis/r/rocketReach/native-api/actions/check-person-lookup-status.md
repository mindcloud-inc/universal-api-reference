# Check Person Lookup Status with RocketReach

Retrieves person lookup status from RocketReach.

## Endpoint

- **Method:** `GET`
- **Path:** `/person/checkStatus`
- **Base URL:** `https://api.rocketreach.co/api/v2`
- **Official documentation:** [Check Person Lookup Status](https://docs.rocketreach.co/reference/rocketreach-check-person-lookup-status-people-lookup-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | query | `string<number>` | no | Comma-separated person lookup IDs to check. Runtime testing on March 16, 2026 confirmed RocketReach accepts a query string like ids=22395600. |
