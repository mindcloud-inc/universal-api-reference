# Create Badge with Absinthe

Creates a new badge in Absinthe.

## Endpoint

- **Method:** `POST`
- **Path:** `/badges`
- **Base URL:** `https://api.absinthe.network`
- **Official documentation:** [Create Badge](https://api.absinthe.network/doc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `badge_name` | body | `string` | no | Name of the badge. |
| `eligibility_dnf` | body | `string` | no | Eligibility definition for the badge. |
