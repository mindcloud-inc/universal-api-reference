# Create Contact with Raklet

## Endpoint

- **Method:** `POST`
- **Path:** `/organisations/:organisationId/contacts`
- **Base URL:** `https://api.raklet.com`
- **Official documentation:** [Create Contact](https://api.raklet.com/swagger/ui/index#/Contact/Contact_Post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `firstName` | body | `string` | yes | Contact first name. |
| `lastName` | body | `string` | yes | Contact last name. |
| `language` | body | `string` | yes | Contact language code. |
