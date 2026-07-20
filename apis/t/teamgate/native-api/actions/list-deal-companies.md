# List Deal Companies with Teamgate

Retrieves companies for a deal in Teamgate.

## Endpoint

- **Method:** `GET`
- **Path:** `/deals/:deal_id/companies`
- **Base URL:** `https://api.teamgate.com/v4`
- **Official documentation:** [List Deal Companies](https://developers.teamgate.com/#c6b214ac-7853-4a7f-8164-bd7bdd91c8fc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deal_id` | path | `string` | yes | Deal ID whose linked companies should be listed. |
