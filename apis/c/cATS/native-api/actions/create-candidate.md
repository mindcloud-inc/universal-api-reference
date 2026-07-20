# Create Candidate with CATS

Creates a new candidate in CATS.

## Endpoint

- **Method:** `POST`
- **Path:** `/candidates`
- **Base URL:** `https://api.catsone.com/v3`
- **Official documentation:** [Create Candidate](https://docs.catsone.com/api/v3/#candidates-create-a-candidate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first_name` | body | `string` | yes | The candidate first name. |
| `last_name` | body | `string` | yes | The candidate last name. |
