# Create Contact with EventGeek

Creates a new contact in EventGeek.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://app.circa.co/api/v1`
- **Official documentation:** [Create Contact](https://docs.circa.co/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Contact email address. |
| `first_name` | body | `string` | yes | Contact first name. |
| `last_name` | body | `string` | yes | Contact last name. |
