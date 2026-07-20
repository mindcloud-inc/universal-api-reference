# Update Person with Makeplans

Updates an existing person in Makeplans.

## Endpoint

- **Method:** `PUT`
- **Path:** `/people/:personId`
- **Base URL:** `https://{accountDomain}/api/v1`
- **Official documentation:** [Update Person](https://developer.makeplans.com/endpoints/people/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `person.email` | body | `string` | no | Person email. |
| `person.name` | body | `string` | no | Person name. |
| `person.phone_number` | body | `string` | no | Person phone number. |
| `personId` | path | `number` | yes | The Makeplans person ID. |
