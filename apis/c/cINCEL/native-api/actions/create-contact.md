# Create Contact with CINCEL

## Endpoint

- **Method:** `POST`
- **Path:** `/teams/:team/contacts`
- **Base URL:** `https://api.cincel.digital/v3`
- **Official documentation:** [Create Contact](https://docs.cincel.digital/v3/digital-signature#post-/teams/-team-/contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team` | path | `string` | yes | UUID of the team that will own the contact. |
| `name` | body | `string` | yes | Name of the contact to create. |
| `email` | body | `string` | yes | Email address of the contact to create. |
