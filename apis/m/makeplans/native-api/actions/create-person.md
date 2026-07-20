# Create Person with Makeplans

Creates a new person in Makeplans.

## Endpoint

- **Method:** `POST`
- **Path:** `/people`
- **Base URL:** `https://{accountDomain}/api/v1`
- **Official documentation:** [Create Person](https://developer.makeplans.com/endpoints/people/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `person.email` | body | `string` | no | Person email. |
| `person.name` | body | `string` | no | Person name. |
| `person.phone_number` | body | `string` | no | Person phone number. |
