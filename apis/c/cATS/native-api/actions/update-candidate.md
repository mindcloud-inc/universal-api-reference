# Update Candidate with CATS

Updates an existing candidate in CATS.

## Endpoint

- **Method:** `PUT`
- **Path:** `/candidates/:id`
- **Base URL:** `https://api.catsone.com/v3`
- **Official documentation:** [Update Candidate](https://docs.catsone.com/api/v3/#candidates-update-a-candidate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The ID of the candidate to update. |
| `first_name` | body | `string` | yes | The candidate first name. |
| `last_name` | body | `string` | yes | The candidate last name. |
