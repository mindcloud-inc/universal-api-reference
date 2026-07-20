# Update Talent with Casting42

Updates an existing talent in Casting42.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v2/talents/update`
- **Base URL:** `https://casting42.com`
- **Official documentation:** [Update Talent](https://documenter.getpostman.com/view/24607394/2s9YR6buRP)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tag` | body | `string` | yes | Unique tag of the talent to update. |
| `lastName` | body | `string` | no | New last name for the talent. |
