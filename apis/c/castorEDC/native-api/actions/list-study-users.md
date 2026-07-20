# List Study Users with Castor EDC

Retrieves study users from Castor EDC by study ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/study/:study_id/user`
- **Base URL:** `https://us.castoredc.com/api`
- **Official documentation:** [List Study Users](https://us.castoredc.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `study_id` | path | `string` | yes | The ID of the study for which this call should be made |
