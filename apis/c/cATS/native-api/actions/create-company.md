# Create Company with CATS

Creates a new company in CATS.

## Endpoint

- **Method:** `POST`
- **Path:** `/companies`
- **Base URL:** `https://api.catsone.com/v3`
- **Official documentation:** [Create Company](https://docs.catsone.com/api/v3/#companies-create-a-company)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The company name. |
| `owner_id` | body | `number` | yes | The owning user ID. |
| `check_duplicate` | query | `boolean` | no | Throw an error instead of creating a duplicate when true. |
