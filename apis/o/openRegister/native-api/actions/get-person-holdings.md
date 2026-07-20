# Get Person Holdings with OpenRegister

Retrieves a person's holdings from OpenRegister.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/person/:person_id/holdings`
- **Base URL:** `https://api.openregister.de`
- **Official documentation:** [Get Person Holdings](https://docs.openregister.de/endpoint/person-holdings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `person_id` | path | `string` | yes | Unique person identifier. |
